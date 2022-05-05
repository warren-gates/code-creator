//[codeCreator](../../../index.md)/[dev.warrengates.codecreator.source.jvmclass](../index.md)/[TypeInfo](index.md)

# TypeInfo

[jvm]\
public final class [TypeInfo](index.md) implements [Type](../-type/index.md)

Implementation of [Type](../-type/index.md) interface

## Parameters

jvm

| | |
|---|---|
| psiType |  |
| factory |  |

## Constructors

| | |
|---|---|
| [TypeInfo](-type-info.md) | [jvm]<br>[TypeInfo](index.md)[TypeInfo](-type-info.md)(PsiTypepsiType, PsiElementFactoryfactory) |

## Functions

| Name | Summary |
|---|---|
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
| [isDouble](is-double.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDouble](is-double.md)()<br>Is double |
| [isFloat](is-float.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFloat](is-float.md)()<br>Is float |
| [isList](is-list.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isList](is-list.md)()<br>Is list |
| [isLong](is-long.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isLong](is-long.md)()<br>Is long |
| [isMap](is-map.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isMap](is-map.md)()<br>Is map |
| [isNestedArray](is-nested-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNestedArray](is-nested-array.md)()<br>Is nested array |
| [isNumeric](is-numeric.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNumeric](is-numeric.md)()<br>Is numeric |
| [isObject](is-object.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObject](is-object.md)()<br>Is object |
| [isObjectArray](is-object-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObjectArray](is-object-array.md)()<br>Is object array |
| [isPrimitive](is-primitive.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitive](is-primitive.md)()<br>Is primitive |
| [isPrimitiveArray](is-primitive-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitiveArray](is-primitive-array.md)()<br>Is primitive array |
| [isSet](is-set.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isSet](is-set.md)()<br>Is set |
| [isShort](is-short.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isShort](is-short.md)()<br>Is short |
| [isString](is-string.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isString](is-string.md)()<br>Is string |
| [isStringArray](is-string-array.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStringArray](is-string-array.md)()<br>Is string array |
| [isVoid](is-void.md) | [jvm]<br>[Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isVoid](is-void.md)()<br>Is void |

## Properties

| Name | Summary |
|---|---|
| [isArray](is-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isArray](is-array.md)<br>Is array |
| [isBoolean](is-boolean.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isBoolean](is-boolean.md)<br>Is boolean |
| [isByte](is-byte.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isByte](is-byte.md)<br>Is byte |
| [isCalendar](is-calendar.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isCalendar](is-calendar.md)<br>Is calendar |
| [isChar](is-char.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isChar](is-char.md)<br>Is char |
| [isCollection](is-collection.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isCollection](is-collection.md)<br>Is collection |
| [isDate](is-date.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDate](is-date.md)<br>Is date |
| [isDouble](is-double.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isDouble](is-double.md)<br>Is double |
| [isFloat](is-float.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isFloat](is-float.md)<br>Is float |
| [isList](is-list.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isList](is-list.md)<br>Is list |
| [isLong](is-long.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isLong](is-long.md)<br>Is long |
| [isMap](is-map.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isMap](is-map.md)<br>Is map |
| [isNestedArray](is-nested-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNestedArray](is-nested-array.md)<br>Is nested array |
| [isNumeric](is-numeric.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isNumeric](is-numeric.md)<br>Is numeric |
| [isObject](is-object.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObject](is-object.md)<br>Is object |
| [isObjectArray](is-object-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isObjectArray](is-object-array.md)<br>Is object array |
| [isPrimitive](is-primitive.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitive](is-primitive.md)<br>Is primitive |
| [isPrimitiveArray](is-primitive-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isPrimitiveArray](is-primitive-array.md)<br>Is primitive array |
| [isSet](is-set.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isSet](is-set.md)<br>Is set |
| [isShort](is-short.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isShort](is-short.md)<br>Is short |
| [isString](is-string.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isString](is-string.md)<br>Is string |
| [isStringArray](is-string-array.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isStringArray](is-string-array.md)<br>Is string array |
| [isVoid](is-void.md) | [jvm]<br>private final [Boolean](https://docs.oracle.com/javase/8/docs/api/java/lang/Boolean.html)[isVoid](is-void.md)<br>Is void |
| [type](index.md#1962405218%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[type](index.md#1962405218%2FProperties%2F-1216412040)<br>Gets type name with package or short name for primitives. Example: for a type of java.lang.String the return value is &quot;java.lang.String&quot;. Primitive example: for an int type the return value is &quot;int&quot;. |
| [typeName](index.md#-359798121%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[typeName](index.md#-359798121%2FProperties%2F-1216412040)<br>Gets type name without package, nulls for primitives. Example: for a type of java.lang.String the return value is &quot;String&quot; |
| [typeQualifiedName](index.md#-129804559%2FProperties%2F-1216412040) | [jvm]<br>private final [String](https://docs.oracle.com/javase/8/docs/api/java/lang/String.html)[typeQualifiedName](index.md#-129804559%2FProperties%2F-1216412040)<br>Gets type qualified name, nulls for primitives. For non-array types this returns the same value as getType(). For array types this returns the same as link{getType()} without trailing brackets. Example: for a type of java.lang.String[] the return value is &quot;java.lang.String&quot; Example: for a type of java.lang.String[][] the return value is &quot;java.lang.String[]&quot; |
