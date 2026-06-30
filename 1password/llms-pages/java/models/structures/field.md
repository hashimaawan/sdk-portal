# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type Object.*


# Class Name

`Field`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Entropy` | `Double` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value | Double getEntropy() | setEntropy(Double entropy) |
| `Generate` | `Boolean` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `false` | Boolean getGenerate() | setGenerate(Boolean generate) |
| `Id` | `String` | Required | - | String getId() | setId(String id) |
| `Label` | `String` | Optional | - | String getLabel() | setLabel(String label) |
| `Purpose` | [`Purpose`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. | Purpose getPurpose() | setPurpose(Purpose purpose) |
| `Recipe` | [`GeneratorRecipe`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value | GeneratorRecipe getRecipe() | setRecipe(GeneratorRecipe recipe) |
| `Section` | [`Section`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/structures/section.md) | Optional | - | Section getSection() | setSection(Section section) |
| `Type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/type-1.md) | Required | **Default**: `Type1.STRING` | Type1 getType() | setType(Type1 type) |
| `Value` | `String` | Optional | - | String getValue() | setValue(String value) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import java.util.Arrays;
import local.m1password.ApiHelper;
import local.m1password.models.CharacterSet;
import local.m1password.models.Field;
import local.m1password.models.GeneratorRecipe;
import local.m1password.models.Purpose;
import local.m1password.models.Type1;

Field field = new Field.Builder(
    "id6",
    Type1.STRING
)
.entropy(80.94D)
.generate(false)
.label("label6")
.purpose(Purpose.NOTES)
.recipe(new GeneratorRecipe.Builder()
        .characterSets(Arrays.asList(
            CharacterSet.LETTERS,
            CharacterSet.SYMBOLS,
            CharacterSet.DIGITS
        ))
        .excludeCharacters("excludeCharacters0")
        .length(64)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
.build();
```



