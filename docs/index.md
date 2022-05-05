## codeCreator

[codeCreator](https://plugins.jetbrains.com/plugin/19097-codecreator) is a general purpose code generator plugin for JetBrains [IntelliJ IDEA][intellij] and [Android Studio][androidStudio] IDEs. It allows for the creation of a code generation task that has one or more [sources](#velocity-context-sources) that can be used in one or more [templates](#velocity-template-sources), with each template having its own output. One example would be to create multiple Thymeleaf files from a Java class.

### Current Features
#### Velocity Context Sources
- A [model](jvmclass/index.html) of the currently open Java or Kotlin class file
- A model of a selected Java or Kotlin class file
- A reference to the currently open [project][project] in the IDE
- A reference to a map of current environment variables retrieved from Java's ```System.getenv()```
- The tools provided by [Velocity Generic Tools][velocityTools]
- The predefined [variables][templateVariables] provided for IntelliJ's File and Code Templates

#### Velocity Template Sources
- String templates added through codeCreator's settings page
- Templates from files

#### Output Targets
- File(s), either by prompting for a file name or by using a template generated file name/path
- The Clipboard


### Use
#### Task Creation
New tasks are created in settings under File -> Settings -> Tools -> codeCreator -> Tasks. The left list pane displays tasks. The '+' button creates a new task, the '-' button deletes the currently selected task, and the wrench button has a dropdown for importing or exporting tasks. To the right of the list pane is a text box for the task's name and tabs for setting Sources and Templates.

Create a new task by clicking the '+' button and give it a unique name. The name is what displays in the IntelliJ/Android Studio Generate list. 

Then add at least one Source by clicking the '+' button on the list in the Sources tab. If desired, change the Source variable name to something more descriptive. Note that each Source must have a unique variable name which must follow Velocity's [naming rules][velocityVariableNaming]. Depending on the specific Source chosen there may be other options available.

Switch to the Templates tab and add a new Template using the '+' button. Currently there are two Template types available: String Templates and Velocity Templates.

String Templates allow you to set a Name, Template text, and Output. For String Templates the Name is only used for display in the Templates list. The Template text box takes your Velocity template text, and Output specifies the desired output target.

To use a Velocity Template you must configure at least one additional ResourceLoader in the codeCreator Properties page under File -> Settings -> Tools -> codeCreator. See [below][#velocity-settings] for more information. Once an additional ResourceLoader is configured you can set Resource Name and Output. Resource Name must match an existing resource that your additional ResourceLoader can find, such as a file name for a configured FileResourceLoader.

#### Running Tasks
Tasks are added to and are run from the IntelliJ/Android Studio Generate... command which is accessed from Code -> Generate... or by hitting Alt-Insert.

### Reference

#### Tasks
A container for Source(s) and Template(s) to be run with the IntelliJ/Android Studio Generate... command. Tasks are context aware, and only show up when they are runnable. As example: a Task with a Current Java/Kotlin File source won't be an option if Generate... is triggered in a text file.

#### Sources
##### Current Java/Kotlin File
This is the open java or kotlin file with focus when triggering the Generate... command. 

##### Selected Java/Kotlin File
This displays a prompt so other project or library class files can be selected.

##### Other Context Sources
As noted [above][#velocity-context-sources], the following additional sources are available in your Velocity templates

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
| Alternator tool | alternator |
| [Value Parser][parser] | parser |
| [List tool][list] | list |
| [Sort tool][sorter] | sorter |
| [Iterator tool][mill] | mill |



#### Templates
##### String Template
Stores the Velocity template text directly

##### Velocity Template
Refers to an external template resource such as a file. Requires that an additional ResourceLoader be [configured][#velocity-settings].

#### Output
##### Clipboard
Template output is copied to clipboard.

##### Selected File
A file selection prompt is display so output can be saved to a file.

##### File Name Template
Allows a file path to be defined as a Velocity template using any of the Sources available, including Task Sources and the [sources][#velocity-context-sources] listed above.  As an example, consider a template that creates a Thymeleaf html page for a specified Java class. Assuming a class named Person with a Source Variable Name of 'class0' in a project located at '/home/warren/myprojects/webproject', the following File Name Template
```velocity
$project.basePath/src/resources/templates/$class0.name/create.html
```
would give an output path of
```
/home/warren/myprojects/webproject/src/resources/templates/Person/create.html
```

File Name Templates has a selection how to handle existing files: Prompt for new name, Overwrite existing file, or Cancel operation. Note that currently Templates are processed sequentially, so it is possible when multiple Templates are used with File Name Templates output with the Cancel option that the first Template processed may save successfully while a subsequent Template may cancel due to an existing file.

#### Velocity Settings
Additional velocity settings can be specified under File -> Settings -> Tools -> codeCreator using property file syntax. This allows you to add additional ResourceLoaders and specify other Velocity runtime configuration. See the Velocity [reference][velocityConfiguration] for specifics. An example of adding a FileResourceLoader would be
```
resource.loader = file
file.resource.loader.description = Velocity File Resource Loader
file.resource.loader.class = org.apache.velocity.runtime.resource.loader.FileResourceLoader
file.resource.loader.path = /path/to/your/template/directory
file.resource.loader.cache = false
file.resource.loader.modificationCheckInterval = 0
```

#### Velocity Library used
codeCreator uses the Velocity library included with IntelliJ/Android Studio, which currently is version 1.7.  For writing templates refer to the [documentation][velocityTemplateReference].

### Roadmap
#### Additional Velocity Context Sources
- [Database metadata][databaseMetadata]
- Other files such as xml, json, csv
- Value(s) collected from a user prompt

#### Additional Velocity Template Sources
- Built in IntelliJ templates

#### Additional Output Targes
- Current Java/Kotlin file



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
[parser]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/ValueParser.html
[list]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/ListTool.html
[sorter]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/SortTool.html
[mill]: https://velocity.apache.org/tools/1.4/javadoc/org/apache/velocity/tools/generic/IteratorTool.html
