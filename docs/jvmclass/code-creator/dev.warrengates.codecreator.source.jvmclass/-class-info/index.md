//[codeCreator](../../../index.md)/[dev.warrengates.codecreator.source.jvmclass](../index.md)/[ClassInfo](index.md)

# ClassInfo

[jvm]\
public final class [ClassInfo](index.md) implements [Visibility](../-visibility/index.md), [AnnotationOwner](../-annotation-owner/index.md)

Information about a java/kotlin class file.

## Parameters

jvm

| | |
|---|---|
| uClass |  |
| fields |  |
| methods |  |

## Constructors

| | |
|---|---|
| [ClassInfo](-class-info.md) | [jvm]<br>[ClassInfo](index.md)[ClassInfo](-class-info.md)(UClassuClass, [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)&lt;UField&gt;fields, [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)&lt;UMethod&gt;methods) |
| [ClassInfo](-class-info.md) | [jvm]<br>[ClassInfo](index.md)[ClassInfo](-class-info.md)(UClassuClass) |

## Functions

| Name | Summary |
|---|---|
| [getAllConstructors](get-all-constructors.md) | [jvm]<br>final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[ConstructorInfo](../-constructor-info/index.md)&gt;[getAllConstructors](get-all-constructors.md)()<br>Get this class's constructors and the constructors of any super classes |
| [getAllFields](get-all-fields.md) | [jvm]<br>final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[FieldInfo](../-field-info/index.md)&gt;[getAllFields](get-all-fields.md)()<br>Get this class's fields and the fields of any super classes |
| [getAllMethods](get-all-methods.md) | [jvm]<br>final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[MethodInfo](../-method-info/index.md)&gt;[getAllMethods](get-all-methods.md)()<br>Get this class's methods and the methods of any super classes |
| [getAnnotations](get-annotations.md) | [jvm]<br>[List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[AnnotationInfo](../-annotation-info/index.md)&gt;[getAnnotations](get-annotations.md)()<br>Annotations |
| [getConstructors](get-constructors.md) | [jvm]<br>final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[ConstructorInfo](../-constructor-info/index.md)&gt;[getConstructors](get-constructors.md)()<br>Get this class's constructors |
| [getFields](get-fields.md) | [jvm]<br>final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[FieldInfo](../-field-info/index.md)&gt;[getFields](get-fields.md)()<br>Get this class's fields |
| [getImplementationNames](get-implementation-names.md) | [jvm]<br>final [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)&lt;[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)&gt;[getImplementationNames](get-implementation-names.md)()<br>Class's implementation names |
| [getMethods](get-methods.md) | [jvm]<br>final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[MethodInfo](../-method-info/index.md)&gt;[getMethods](get-methods.md)()<br>Get this class's methods |
| [getName](get-name.md) | [jvm]<br>final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getName](get-name.md)()<br>The class's name |
| [getQualifiedName](get-qualified-name.md) | [jvm]<br>final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getQualifiedName](get-qualified-name.md)()<br>The class's qualified name, will be null for anonymous and local classes as well as type parameters |
| [getSuperClass](get-super-class.md) | [jvm]<br>final [ClassInfo](index.md)[getSuperClass](get-super-class.md)()<br>The class's super class, if it exists |
| [isAbstract](is-abstract.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isAbstract](is-abstract.md)()<br>Class is abstract |
| [isDeprecated](is-deprecated.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDeprecated](is-deprecated.md)()<br>Class is deprecated |
| [isEnum](is-enum.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isEnum](is-enum.md)()<br>Class is an enum |
| [isException](is-exception.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isException](is-exception.md)()<br>Class is an exception |
| [isFinal](is-final.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFinal](is-final.md)()<br>Class is final |
| [isPackageLocal](is-package-local.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPackageLocal](is-package-local.md)()<br>Is package local |
| [isPrivate](is-private.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrivate](is-private.md)()<br>Is private |
| [isProtected](is-protected.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isProtected](is-protected.md)()<br>Is protected |
| [isPublic](is-public.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPublic](is-public.md)()<br>Is public |
| [isRecord](is-record.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isRecord](is-record.md)()<br>Class is a record |
| [isStatic](is-static.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStatic](is-static.md)()<br>Class is static |
| [toString](to-string.md) | [jvm]<br>[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[toString](to-string.md)() |

## Properties

| Name | Summary |
|---|---|
| [annotations](../-parameter-info/index.md#639399274%2FProperties%2F-1216412040) | [jvm]<br>private final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[AnnotationInfo](../-annotation-info/index.md)&gt;[annotations](../-parameter-info/index.md#639399274%2FProperties%2F-1216412040)<br>Annotations |
| [implementationNames](index.md#936264534%2FProperties%2F-1216412040) | [jvm]<br>private final [Array](https://kotlinlang.org/api/latest/jvm/stdlib/kotlin/-array/index.html)&lt;[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)&gt;[implementationNames](index.md#936264534%2FProperties%2F-1216412040)<br>Class's implementation names |
| [isAbstract](is-abstract.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isAbstract](is-abstract.md)<br>Class is abstract |
| [isDeprecated](is-deprecated.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDeprecated](is-deprecated.md)<br>Class is deprecated |
| [isEnum](is-enum.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isEnum](is-enum.md)<br>Class is an enum |
| [isException](is-exception.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isException](is-exception.md)<br>Class is an exception |
| [isFinal](is-final.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFinal](is-final.md)<br>Class is final |
| [isPackageLocal](../-visibility/is-package-local.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPackageLocal](../-visibility/is-package-local.md)<br>Is package local |
| [isPrivate](../-visibility/is-private.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrivate](../-visibility/is-private.md)<br>Is private |
| [isProtected](../-visibility/is-protected.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isProtected](../-visibility/is-protected.md)<br>Is protected |
| [isPublic](../-visibility/is-public.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPublic](../-visibility/is-public.md)<br>Is public |
| [isRecord](is-record.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isRecord](is-record.md)<br>Class is a record |
| [isStatic](is-static.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStatic](is-static.md)<br>Class is static |
| [name](index.md#2053209571%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[name](index.md#2053209571%2FProperties%2F-1216412040)<br>The class's name |
| [qualifiedName](index.md#932362533%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[qualifiedName](index.md#932362533%2FProperties%2F-1216412040)<br>The class's qualified name, will be null for anonymous and local classes as well as type parameters |
| [superClass](index.md#407778609%2FProperties%2F-1216412040) | [jvm]<br>private final [ClassInfo](index.md)[superClass](index.md#407778609%2FProperties%2F-1216412040)<br>The class's super class, if it exists |
