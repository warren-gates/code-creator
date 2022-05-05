//[codeCreator](../../../index.md)/[dev.warrengates.codecreator.source.jvmclass](../index.md)/[MethodInfo](index.md)

# MethodInfo

[jvm]\
public final class [MethodInfo](index.md) implements [Type](../-type/index.md), [Visibility](../-visibility/index.md), [Parameterized](../-parameterized/index.md), [AnnotationOwner](../-annotation-owner/index.md)

Information about a java/kotlin class's methods.

## Parameters

jvm

| | |
|---|---|
| method |  |

## Constructors

| | |
|---|---|
| [MethodInfo](-method-info.md) | [jvm]<br>[MethodInfo](index.md)[MethodInfo](-method-info.md)(UMethodmethod) |

## Functions

| Name | Summary |
|---|---|
| [getAnnotations](get-annotations.md) | [jvm]<br>[List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[AnnotationInfo](../-annotation-info/index.md)&gt;[getAnnotations](get-annotations.md)()<br>Annotations |
| [getFieldName](get-field-name.md) | [jvm]<br>final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getFieldName](get-field-name.md)()<br>Returns the name of the backing field if this method is a getter or setter, otherwise returns null |
| [getName](get-name.md) | [jvm]<br>final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getName](get-name.md)()<br>Method's name |
| [getParameters](get-parameters.md) | [jvm]<br>[List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[ParameterInfo](../-parameter-info/index.md)&gt;[getParameters](get-parameters.md)()<br>Parameters |
| [getType](get-type.md) | [jvm]<br>[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getType](get-type.md)()<br>Gets type name with package or short name for primitives. Example: for a type of java.lang.String the return value is &quot;java.lang.String&quot;. Primitive example: for an int type the return value is &quot;int&quot;. |
| [getTypeName](get-type-name.md) | [jvm]<br>[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getTypeName](get-type-name.md)()<br>Gets type name without package, nulls for primitives. Example: for a type of java.lang.String the return value is &quot;String&quot; |
| [getTypeQualifiedName](get-type-qualified-name.md) | [jvm]<br>[String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[getTypeQualifiedName](get-type-qualified-name.md)()<br>Gets type qualified name, nulls for primitives. For non-array types this returns the same value as getType(). For array types this returns the same as link{getType()} without trailing brackets. Example: for a type of java.lang.String[] the return value is &quot;java.lang.String&quot; Example: for a type of java.lang.String[][] the return value is &quot;java.lang.String[]&quot; |
| [isArray](is-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isArray](is-array.md)()<br>Is array |
| [isBoolean](is-boolean.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isBoolean](is-boolean.md)()<br>Is boolean |
| [isByte](is-byte.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isByte](is-byte.md)()<br>Is byte |
| [isCalendar](is-calendar.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isCalendar](is-calendar.md)()<br>Is calendar |
| [isChar](is-char.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isChar](is-char.md)()<br>Is char |
| [isCollection](is-collection.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isCollection](is-collection.md)()<br>Is collection |
| [isDate](is-date.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDate](is-date.md)()<br>Is date |
| [isDeprecated](is-deprecated.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDeprecated](is-deprecated.md)()<br>Method is deprecated |
| [isDouble](is-double.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDouble](is-double.md)()<br>Is double |
| [isFinal](is-final.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFinal](is-final.md)()<br>Method is final |
| [isFloat](is-float.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFloat](is-float.md)()<br>Is float |
| [isGetter](is-getter.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isGetter](is-getter.md)()<br>Method is a getter |
| [isList](is-list.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isList](is-list.md)()<br>Is list |
| [isLong](is-long.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isLong](is-long.md)()<br>Is long |
| [isMap](is-map.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isMap](is-map.md)()<br>Is map |
| [isModifierAbstract](is-modifier-abstract.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isModifierAbstract](is-modifier-abstract.md)()<br>Method is marked as abstract |
| [isModifierSynchronized](is-modifier-synchronized.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isModifierSynchronized](is-modifier-synchronized.md)()<br>Method is marked as synchronized |
| [isNestedArray](is-nested-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNestedArray](is-nested-array.md)()<br>Is nested array |
| [isNumeric](is-numeric.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNumeric](is-numeric.md)()<br>Is numeric |
| [isObject](is-object.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObject](is-object.md)()<br>Is object |
| [isObjectArray](is-object-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObjectArray](is-object-array.md)()<br>Is object array |
| [isPackageLocal](is-package-local.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPackageLocal](is-package-local.md)()<br>Is package local |
| [isPrimitive](is-primitive.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitive](is-primitive.md)()<br>Is primitive |
| [isPrimitiveArray](is-primitive-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitiveArray](is-primitive-array.md)()<br>Is primitive array |
| [isPrivate](is-private.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrivate](is-private.md)()<br>Is private |
| [isProtected](is-protected.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isProtected](is-protected.md)()<br>Is protected |
| [isPublic](is-public.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPublic](is-public.md)()<br>Is public |
| [isReturnTypeVoid](is-return-type-void.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isReturnTypeVoid](is-return-type-void.md)()<br>Method's return type is void |
| [isSet](is-set.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isSet](is-set.md)()<br>Is set |
| [isSetter](is-setter.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isSetter](is-setter.md)()<br>Method is a setter |
| [isShort](is-short.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isShort](is-short.md)()<br>Is short |
| [isStatic](is-static.md) | [jvm]<br>final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStatic](is-static.md)()<br>Method is static |
| [isString](is-string.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isString](is-string.md)()<br>Is string |
| [isStringArray](is-string-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStringArray](is-string-array.md)()<br>Is string array |
| [isVoid](is-void.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isVoid](is-void.md)()<br>Is void |

## Properties

| Name | Summary |
|---|---|
| [annotations](../-parameter-info/index.md#639399274%2FProperties%2F-1216412040) | [jvm]<br>private final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[AnnotationInfo](../-annotation-info/index.md)&gt;[annotations](../-parameter-info/index.md#639399274%2FProperties%2F-1216412040)<br>Annotations |
| [fieldName](index.md#-755790222%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[fieldName](index.md#-755790222%2FProperties%2F-1216412040)<br>Returns the name of the backing field if this method is a getter or setter, otherwise returns null |
| [isArray](../-type/is-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isArray](../-type/is-array.md)<br>Is array |
| [isBoolean](../-type/is-boolean.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isBoolean](../-type/is-boolean.md)<br>Is boolean |
| [isByte](../-type/is-byte.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isByte](../-type/is-byte.md)<br>Is byte |
| [isCalendar](../-type/is-calendar.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isCalendar](../-type/is-calendar.md)<br>Is calendar |
| [isChar](../-type/is-char.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isChar](../-type/is-char.md)<br>Is char |
| [isCollection](../-type/is-collection.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isCollection](../-type/is-collection.md)<br>Is collection |
| [isDate](../-type/is-date.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDate](../-type/is-date.md)<br>Is date |
| [isDeprecated](is-deprecated.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDeprecated](is-deprecated.md)<br>Method is deprecated |
| [isDouble](../-type/is-double.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDouble](../-type/is-double.md)<br>Is double |
| [isFinal](is-final.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFinal](is-final.md)<br>Method is final |
| [isFloat](../-type/is-float.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFloat](../-type/is-float.md)<br>Is float |
| [isGetter](is-getter.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isGetter](is-getter.md)<br>Method is a getter |
| [isList](../-type/is-list.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isList](../-type/is-list.md)<br>Is list |
| [isLong](../-type/is-long.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isLong](../-type/is-long.md)<br>Is long |
| [isMap](../-type/is-map.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isMap](../-type/is-map.md)<br>Is map |
| [isModifierAbstract](is-modifier-abstract.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isModifierAbstract](is-modifier-abstract.md)<br>Method is marked as abstract |
| [isModifierSynchronized](is-modifier-synchronized.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isModifierSynchronized](is-modifier-synchronized.md)<br>Method is marked as synchronized |
| [isNestedArray](../-type/is-nested-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNestedArray](../-type/is-nested-array.md)<br>Is nested array |
| [isNumeric](../-type/is-numeric.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNumeric](../-type/is-numeric.md)<br>Is numeric |
| [isObject](../-type/is-object.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObject](../-type/is-object.md)<br>Is object |
| [isObjectArray](../-type/is-object-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObjectArray](../-type/is-object-array.md)<br>Is object array |
| [isPackageLocal](../-visibility/is-package-local.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPackageLocal](../-visibility/is-package-local.md)<br>Is package local |
| [isPrimitive](../-type/is-primitive.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitive](../-type/is-primitive.md)<br>Is primitive |
| [isPrimitiveArray](../-type/is-primitive-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitiveArray](../-type/is-primitive-array.md)<br>Is primitive array |
| [isPrivate](../-visibility/is-private.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrivate](../-visibility/is-private.md)<br>Is private |
| [isProtected](../-visibility/is-protected.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isProtected](../-visibility/is-protected.md)<br>Is protected |
| [isPublic](../-visibility/is-public.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPublic](../-visibility/is-public.md)<br>Is public |
| [isReturnTypeVoid](is-return-type-void.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isReturnTypeVoid](is-return-type-void.md)<br>Method's return type is void |
| [isSet](../-type/is-set.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isSet](../-type/is-set.md)<br>Is set |
| [isSetter](is-setter.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isSetter](is-setter.md)<br>Method is a setter |
| [isShort](../-type/is-short.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isShort](../-type/is-short.md)<br>Is short |
| [isStatic](is-static.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStatic](is-static.md)<br>Method is static |
| [isString](../-type/is-string.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isString](../-type/is-string.md)<br>Is string |
| [isStringArray](../-type/is-string-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStringArray](../-type/is-string-array.md)<br>Is string array |
| [isVoid](../-type/is-void.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isVoid](../-type/is-void.md)<br>Is void |
| [name](index.md#1596540312%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[name](index.md#1596540312%2FProperties%2F-1216412040)<br>Method's name |
| [parameters](index.md#1931376279%2FProperties%2F-1216412040) | [jvm]<br>private final [List](https://docs.oracle.com/javase/8/docs/api/java/util/List.html)&lt;[ParameterInfo](../-parameter-info/index.md)&gt;[parameters](index.md#1931376279%2FProperties%2F-1216412040)<br>Parameters |
| [type](../-parameter-info/index.md#300777748%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[type](../-parameter-info/index.md#300777748%2FProperties%2F-1216412040)<br>Gets type name with package or short name for primitives. Example: for a type of java.lang.String the return value is &quot;java.lang.String&quot;. Primitive example: for an int type the return value is &quot;int&quot;. |
| [typeName](../-parameter-info/index.md#642667849%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[typeName](../-parameter-info/index.md#642667849%2FProperties%2F-1216412040)<br>Gets type name without package, nulls for primitives. Example: for a type of java.lang.String the return value is &quot;String&quot; |
| [typeQualifiedName](../-parameter-info/index.md#946525311%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[typeQualifiedName](../-parameter-info/index.md#946525311%2FProperties%2F-1216412040)<br>Gets type qualified name, nulls for primitives. For non-array types this returns the same value as getType(). For array types this returns the same as link{getType()} without trailing brackets. Example: for a type of java.lang.String[] the return value is &quot;java.lang.String&quot; Example: for a type of java.lang.String[][] the return value is &quot;java.lang.String[]&quot; |
