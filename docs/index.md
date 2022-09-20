# codeCreator

[codeCreator](https://plugins.jetbrains.com/plugin/19097-codecreator) is a general purpose code generator plugin for JetBrains [IntelliJ IDEA][intellij] and [Android Studio][androidStudio] IDEs. It allows for the creation of a code generation task that has one or more [sources](#velocity-context-sources) that can be used in one or more [templates](#velocity-template-sources), with each template having its own output. One example would be to create multiple Thymeleaf files from a Java class.

## Latest Additions
- [Current method](#current-method) as template source
- [Caret location](#caret) as output target


## Current Features
### Velocity Context Sources
- [Database metadata](#database-metadata) from a connected JDBC database
- A [model](#current-javakotlin-file) of the currently open Java or Kotlin class file
- A [model](#selected-javakotlin-file) of a selected Java or Kotlin class file
- A reference to the currently open [project][project] in the IDE
- A reference to a map of current environment variables retrieved from Java's ```System.getenv()```
- The tools provided by [Velocity Generic Tools](#other-context-sources)
- The predefined [variables][templateVariables] provided for IntelliJ's File and Code Templates

### Velocity Template Sources
- String templates added through codeCreator's settings page
- Templates from files
- IntelliJ Include templates

### Output Targets
- File(s), either by prompting for a file name or by using a template generated file name/path
- The Clipboard
- Caret


## Use
### Task Creation
New tasks are created in settings under File -> Settings -> Tools -> codeCreator -> Tasks. The left list pane displays tasks. The '+' button creates a new task, the '-' button deletes the currently selected task, and the wrench button has a dropdown for importing or exporting tasks. To the right of the list pane is a text box for the task's name and tabs for setting Sources and Templates.

Create a new task by clicking the '+' button and give it a unique name. The name is what displays in the IntelliJ/Android Studio Generate list. 

Then add at least one Source by clicking the '+' button on the list in the Sources tab. If desired, change the Source variable name to something more descriptive. Note that each Source must have a unique variable name which must follow Velocity's [naming rules][velocityVariableNaming]. Depending on the specific Source chosen there may be other options available.

Switch to the Templates tab and add a new Template using the '+' button. Currently there are two Template types available: String Templates and Velocity Templates.

String Templates allow you to set a Name, Template text, and Output. For String Templates the Name is only used for display in the Templates list. The Template text box takes your Velocity template text, and Output specifies the desired output target.

To use a Velocity Template you must configure at least one additional ResourceLoader in the codeCreator Properties page under File -> Settings -> Tools -> codeCreator. See [below](#velocity-settings) for more information. Once an additional ResourceLoader is configured you can set Resource Name and Output. Resource Name must match an existing resource that your additional ResourceLoader can find, such as a file name for a configured FileResourceLoader.

### Running Tasks
Tasks are added to and are run from the IntelliJ/Android Studio Generate... command which is accessed from Code -> Generate... or by hitting Alt-Insert.

## Reference

### Tasks
A container for Source(s) and Template(s) to be run with the IntelliJ/Android Studio Generate... command. Tasks are context aware, and only show up when they are runnable. As example: a Task with a Current Java/Kotlin File source won't be an option if Generate... is triggered in a text file.

### Sources
#### Database Metadata
This connects to a specified database and provides a [wrapper][databaseMetadata] around Java's [DatabaseMetaData][jdkMetadata] interface. 

Quick start:
- Add appropriate driver jar under Drivers (IntelliJ Settings -> Tools -> codeCreator -> Drivers tab)
- Optionally add a saved connection (you can also configure your task to prompt for connection info)
- Review [better-metadata][databaseMetadata] api for usage in velocity template
- Create task as described above and add Database Metadata as a Source
- See below for important notes regarding [Drivers](#drivers) and [Connections](#connections)

The database metadata source editor allows you to choose the velocity variable name, pick either a stored or prompted connection, and filter on catalog and schema. The catalog and schema filters act as defaults on the [Database](https://warren-gates.github.io/better-metadata/javadoc/dev/warrengates/bettermetadata/Database.html) object and apply to any of its filterable method calls unless overridden. The catalog/schema filters work as follows:

- Unchecked: no filtering
- Checked with empty textbox: retrieves items without catalog/schema
- Checked with text in textbox: retrieves items matching specified catalog/schema. Note that the text must match an existing catalog, there is no wildcard matching. Schema can use wildcard matching, where '%' matches and substring of zero or more characters, and '_' matches any single character. See details at the top of the [DatabaseMetaData page][jdkMetadata].

Examples using schema only (applies similarly to catalog): 
Variable name: `db`

schema filter unchecked
```java
db.getTables() // retrieves all tables in database available to logged in user
```

schema filters checked with blank textbox
```java
db.getTables() // retrieves all tables without schema in database available to logged in user
```

schema filters checked with textbox = 'public'
```java
db.getTables() // retrieves all tables where schema equals 'public' in database available to logged in user

// note that the default filter can be overridden if schema is passed to getTables method with signature
// getTables(String catalog, String schemaPattern, String tableNamePattern, Array<String> types)
db.getTables(null, "otherSchema", null, null) // retrieves all tables where schema equals 'otherSchema' in database available to logged in user
```

Currently there is no user interface for filtering of database objects such as tables or procedures. Filters can applied in method calls, with most relevant methods including a signature that just takes a name pattern, using the wildcard rules noted above. As an example:
```java
db.getTables("employee%") // would return tables named 'employee', 'employeetype', etc.
db.getTables("employee") // would only return a table named 'employee', if it exists
```

IMPORTANT DATABASE METADATA NOTES
- This is a wrapper around the Java [DatabaseMetaData][jdkMetadata] interface and provides no additional error handling. If a call to DatabaseMetaData throws an exception then this wrapper will throw the same exception.
- The returned metadata will be limited by the logged in user's permissions
- Not every database driver handles every request correctly. During testing I found that the MariaDB driver returns schema information from the `getCatalogs()` method. Unexpected results may very well be coming from the underlying driver.



##### Drivers
Drivers can be added by choosing a jar file on your local filesystem or by downloading from Maven Central. 

To add a local jar click the add button on the list under the Drivers tab (Settings -> Tools -> codeCreator), choose a name, and browse to the jar file you wish to add. Once a jar file is selected and classes that implement the java.sql.Driver interface will show in the Driver Class dropdown. If necessary, select the appropriate class. Click Apply or OK to save the driver information.

If you want to download a driver, you MUST set and apply the Local repo path first. An existing Maven repository path can be used. Once the local repo path is set, you can add a driver using the From Repository option. This differs from the local jar instruction above by asking for download coordinates instead of a file path. The coordinates are in the Maven format of

```maven
groupID:artifactId:verson
```

using MariaDB version 3.07 as an example would give coordinates of

```maven
org.mariadb.jdbc:mariadb-java-client:3.0.7
```
An easy way to get the correct coordinates is to copy them from [mvnrepository.com](https://mvnrepository.com/). If you have selected an existing local Maven repository for the local repo path, that repository will be checked to see if a driver jar matching the coordinates already exists. If it does the Download button will be disabled and a message displayed indicating that a match was found locally. Otherwise, click the Download button to download the driver jar from Maven Central. Once downloaded the Driver Class dropdown will be populated as noted above. Select the desired driver class and save.

IMPORTANT DRIVER NOTES
- Set and Apply Local repo path before downloading drivers
- Note that drivers are downloaded from Maven Central, an option to use other remote repositories will be added shortly
- You will need to choose the correct driver class (if multiples exist). Refer to the specific driver's documentation to pick the correct class

##### Connections
To create a stored connection, go to Settings -> Tools -> codeCreator -> Connections tab. Click the add button, enter a name, choose a Driver, enter a URL, and optionally a username and password. Passwords are stored using IntelliJ's [Sensitive Data API][sensitiveData]. As an alternative to a stored connection, during task creation you can specify a connection prompt each time the task is run. 


#### Current Java/Kotlin File
This is the open java or kotlin file with focus when triggering the Generate... command. Javadoc [here][jvmclassPackageSummary]

#### Selected Java/Kotlin File
This displays a prompt so other project or library class files can be selected. Javadoc [here][jvmclassPackageSummary]

#### IntelliJ Includes templates
You can now use templates defined in Settings -> Editor -> File and Code Templates, Includes by adding an `#parse` or `#include` statement in your existing templates. Using the existing "File Header" template as example:

If your "File Header" contains its own velocity template language, such as ${USER}, you would include it in a codeCreator template with the `#parse` statement
```
#parse("File Header")
```

if your "File Header" does not contain any velocity template language, it would be included in a codeCreator template with the `#include` statement
```
#include("File Header")
```

Not that individual IntelliJ Includes templates will not be loaded if their name conflicts with an existing codeCreator context source.  For more details on the `#include` and `#parse` statements see the [Velocity Documentation][indludeStatement].

#### Current Method
The [method][methodInfo] that contains the caret. 

#### Other Context Sources
As noted [above](#velocity-context-sources), the following additional sources are available in your Velocity templates

The predefined [variables][templateVariables] provided for IntelliJ's File and Code Templates
and the following

| Source | variable name |
| --- | --- |
| reference to current [project][project] | project |
| map of environment variables | env |
| [Date tool][date] | date |
| [Math tool][math] | math |
| [Number tool][number] | number |
| [Render tool][render] | render |
| [Escape tool][esc] | esc |
| [Resource tool][text] | text |
| [Alternator tool][alternator] | alternator |
| [Value Parser][parser] | parser |
| [List tool][list] | list |
| [Sort tool][sorter] | sorter |
| [Iterator tool][mill] | mill |



### Templates
#### String Template
Stores the Velocity template text directly

#### Velocity Template
Refers to an external template file resource. Requires that an additional ResourceLoader be [configured](#velocity-settings). When using an external file, the Resource Name specified in the settings dialog is the path of the file relative to the resource loader path specified in the [Velocity Properties](#velocity-settings). As an example, assuming the Velocity Properties shown below, for a template file whose full path is '/path/to/your/template/directory/sometemplate.vm', the Resource Name would be 'sometemplate.vm'. In other words, the resource loader path specified in Velocity Properties is concatenated with the Resource Name in the Velocity Template editor to get the full path to the template file.

### Output
#### Clipboard
Template output is copied to clipboard.

#### Selected File
A file selection prompt is display so output can be saved to a file.

#### File Name Template
Allows a file path to be defined as a Velocity template using any of the Sources available, including Task Sources and the [sources](#velocity-context-sources) listed above.  As an example, consider a template that creates a Thymeleaf html page for a specified Java class. Assuming a class named Person with a Source Variable Name of 'class0' in a project located at '/home/warren/myprojects/webproject', the following File Name Template
```velocity
$project.basePath/src/resources/templates/$class0.name/create.html
```
would give an output path of
```
/home/warren/myprojects/webproject/src/resources/templates/Person/create.html
```

File Name Templates has a selection how to handle existing files: Prompt for new name, Overwrite existing file, or Cancel operation. Note that currently Templates are processed sequentially, so it is possible when multiple Templates are used with File Name Templates output with the Cancel option that the first Template processed may save successfully while a subsequent Template may cancel due to an existing file.

#### Caret
Template output is placed at current caret location. If an area is selected it will be replaced by the template output.

### Velocity Settings
Additional velocity settings can be specified under File -> Settings -> Tools -> codeCreator, Velocity Properties using property file syntax. This allows you to add additional ResourceLoaders and specify other Velocity runtime configuration. See the Velocity [reference][velocityConfiguration] for specifics. An example of adding a FileResourceLoader would be
```
resource.loader = file
file.resource.loader.description = Velocity File Resource Loader
file.resource.loader.class = org.apache.velocity.runtime.resource.loader.FileResourceLoader
file.resource.loader.path = /path/to/your/template/directory
file.resource.loader.cache = false
file.resource.loader.modificationCheckInterval = 0
```

### Velocity Library used
codeCreator uses the Velocity library included with IntelliJ/Android Studio, which currently is version 1.7.  For writing templates refer to the [documentation][velocityTemplateReference].

## Roadmap
### Additional Velocity Context Sources
- Other files such as xml, json, csv
- Value(s) collected from a user prompt

### Additional Velocity Template Sources
- Built in IntelliJ templates

### Additional Output Targes
- Current Java/Kotlin file


[jvmclassPackageSummary]: jvmclass/dev/warrengates/codecreator/source/jvmclass/package-summary.html
[intellij]: https://www.jetbrains.com/idea/
[androidStudio]: https://developer.android.com/studio/
[project]: https://github.com/JetBrains/intellij-community/blob/3a43e28a7925ba02ab4d8bd8131a22c0d8a54dfd/platform/core-api/src/com/intellij/openapi/project/Project.java
[velocityTools]: https://velocity.apache.org/tools/1.4/generic/index.html
[templateVariables]: https://www.jetbrains.com/help/idea/file-template-variables.html
[databaseMetadata]: https://warren-gates.github.io/better-metadata/
[velocityVariableNaming]: https://velocity.apache.org/engine/1.7/user-guide.html#variables
[velocityTemplateReference]: https://velocity.apache.org/engine/1.7/developer-guide.html#velocity-configuration-keys-and-values
[velocityConfiguration]: https://velocity.apache.org/engine/1.7/developer-guide.html#velocity-configuration-keys-and-values
[date]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/DateTool.html
[math]: https://velocity.apache.org/tools/1.4/generic/MathTool.html
[number]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/NumberTool.html
[render]: https://velocity.apache.org/tools/1.4/generic/RenderTool.html
[esc]: https://velocity.apache.org/tools/1.4/generic/EscapeTool.html
[text]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/ResourceTool.html
[alternator]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/AlternatorTool.html
[parser]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/ValueParser.html
[list]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/ListTool.html
[sorter]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/SortTool.html
[mill]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/IteratorTool.html
[jdkMetadata]: https://docs.oracle.com/en/java/javase/17/docs/api/java.sql/java/sql/DatabaseMetaData.html
[sensitiveData]: https://plugins.jetbrains.com/docs/intellij/persisting-sensitive-data.html
[indludeStatement]: https://velocity.apache.org/engine/1.7/user-guide.html#include
[methodInfo]: jvmclass/dev/warrengates/codecreator/source/jvmclass/MethodInfo.html
