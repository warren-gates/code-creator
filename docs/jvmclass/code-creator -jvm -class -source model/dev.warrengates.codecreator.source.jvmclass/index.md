//[codeCreator Jvm Class Source model](../../index.md)/[dev.warrengates.codecreator.source.jvmclass](index.md)

# Package dev.warrengates.codecreator.source.jvmclass

## Types

| Name | Summary |
|---|---|
| [AnnotationInfo](-annotation-info/index.md) | [jvm]<br>public final class [AnnotationInfo](-annotation-info/index.md)<br>Information about an annotation used on a type, field, method, or parameter |
| [AnnotationInfoList](-annotation-info-list/index.md) | [jvm]<br>public final class [AnnotationInfoList](-annotation-info-list/index.md) implements [AnnotationOwner](-annotation-owner/index.md)<br>Convenience class for holding a list of [AnnotationInfo](-annotation-info/index.md) objects |
| [AnnotationOwner](-annotation-owner/index.md) | [jvm]<br>public interface [AnnotationOwner](-annotation-owner/index.md)<br>Convenience interface for reusing [AnnotationInfoList](-annotation-info-list/index.md) |
| [ClassInfo](-class-info/index.md) | [jvm]<br>public final class [ClassInfo](-class-info/index.md) implements [Visibility](-visibility/index.md), [AnnotationOwner](-annotation-owner/index.md)<br>Information about a java/kotlin class file. |
| [ConstructorInfo](-constructor-info/index.md) | [jvm]<br>public final class [ConstructorInfo](-constructor-info/index.md) implements [Parameterized](-parameterized/index.md), [Visibility](-visibility/index.md)<br>Information about a java/kotlin class's constructor. |
| [FieldInfo](-field-info/index.md) | [jvm]<br>public final class [FieldInfo](-field-info/index.md) implements [Type](-type/index.md), [Visibility](-visibility/index.md), [AnnotationOwner](-annotation-owner/index.md)<br>Information about a java/kotlin class's fields. |
| [MethodInfo](-method-info/index.md) | [jvm]<br>public final class [MethodInfo](-method-info/index.md) implements [Type](-type/index.md), [Visibility](-visibility/index.md), [Parameterized](-parameterized/index.md), [AnnotationOwner](-annotation-owner/index.md)<br>Information about a java/kotlin class's methods. |
| [ParameterInfo](-parameter-info/index.md) | [jvm]<br>public final class [ParameterInfo](-parameter-info/index.md) implements [Type](-type/index.md), [AnnotationOwner](-annotation-owner/index.md)<br>Information about a method's or constructor's parameters. |
| [ParameterInfoList](-parameter-info-list/index.md) | [jvm]<br>public final class [ParameterInfoList](-parameter-info-list/index.md) implements [Parameterized](-parameterized/index.md)<br>Convenience class for holding a list of [ParameterInfo](-parameter-info/index.md) objects |
| [Parameterized](-parameterized/index.md) | [jvm]<br>public interface [Parameterized](-parameterized/index.md)<br>Convenience interface for reusing [ParameterInfoList](-parameter-info-list/index.md) |
| [Type](-type/index.md) | [jvm]<br>public interface [Type](-type/index.md)<br>Type |
| [TypeInfo](-type-info/index.md) | [jvm]<br>public final class [TypeInfo](-type-info/index.md) implements [Type](-type/index.md)<br>Implementation of [Type](-type/index.md) interface |
| [Visibility](-visibility/index.md) | [jvm]<br>public interface [Visibility](-visibility/index.md)<br>Information about an object's visibility |
| [VisibilityInfo](-visibility-info/index.md) | [jvm]<br>public final class [VisibilityInfo](-visibility-info/index.md) implements [Visibility](-visibility/index.md)<br>Implementation of [Visibility](-visibility/index.md) interface |
