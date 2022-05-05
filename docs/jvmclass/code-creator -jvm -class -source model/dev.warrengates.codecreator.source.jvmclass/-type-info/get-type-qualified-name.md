//[codeCreator Jvm Class Source model](../../../index.md)/[dev.warrengates.codecreator.source.jvmclass](../index.md)/[TypeInfo](index.md)/[getTypeQualifiedName](get-type-qualified-name.md)

# getTypeQualifiedName

[jvm]\

[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getTypeQualifiedName](get-type-qualified-name.md)()

Gets type qualified name, nulls for primitives. For non-array types this returns the same value as getType(). For array types this returns the same as link{getType()} without trailing brackets. Example: for a type of java.lang.String[] the return value is &quot;java.lang.String&quot; Example: for a type of java.lang.String[][] the return value is &quot;java.lang.String[]&quot;

#### Return

the type qualified name
