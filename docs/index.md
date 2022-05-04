## codeCreator documentation

[codeCreator](https://plugins.jetbrains.com/plugin/19097-codecreator) is a general purpose code generator plugin for JetBrains [IntelliJ IDEA][intellij] and [Android Studio][androidStudio] IDEs. It allows the creation of a code generation task that allows for one or more [sources](#sources) that can be used in one or more [templates](#templates). One example would be to create multiple Thymeleaf files from a Java class.

#### Current Features
##### Velocity Context Sources {#sources}
- A model of the currently open Java or Kotlin class file
- A model of a selected Java or Kotlin class file
- A reference to the currently open [project][project] in the IDE
- A reference to a map of current envronment variables retrieved from Java's ```System.getenv()```
- The tools provided by [Velocity Generic Tools][velocityTools]
- The predefined [variables][templateVariables] provided for IntelliJ's File and Code Templates

##### Velocity Template Sources {#templates}
- String templates added through codeCreator's settings page
- Templates from files

##### Output Targets
- File(s), either by prompting for a file name or by using a template generated file name/path
- The Clipboard


#### Use

#### Reference
##### Velocity

##### Context Sources

#### Roadmap
##### Additional Velocity Context Sources
- [Database metadata][databaseMetadata]
- Other files such as xml, json, csv
- Value(s) collected from a user prompt

##### Additional Velocity Template Sources
- Built in IntelliJ templates

##### Additional Output Targes
- Current Java/Kotlin file



[intellij]: https://www.jetbrains.com/idea/
[androidStudio]: https://developer.android.com/studio/
[project]: https://github.com/JetBrains/intellij-community/blob/3a43e28a7925ba02ab4d8bd8131a22c0d8a54dfd/platform/core-api/src/com/intellij/openapi/project/Project.java
[velocityTools]: https://velocity.apache.org/tools/1.4/generic/index.html
[templateVariables]: https://www.jetbrains.com/help/idea/file-template-variables.html
[databaseMetadata]: https://github.com/warren-gates/better-metadata
