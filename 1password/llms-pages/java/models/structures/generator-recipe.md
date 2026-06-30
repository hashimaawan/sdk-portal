# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/java/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type Object.*


# Class Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `CharacterSets` | [`List<CharacterSet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/java/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* | List<CharacterSet> getCharacterSets() | setCharacterSets(List<CharacterSet> characterSets) |
| `ExcludeCharacters` | `String` | Optional | List of all characters that should be excluded from generated passwords. | String getExcludeCharacters() | setExcludeCharacters(String excludeCharacters) |
| `Length` | `Integer` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` | Integer getLength() | setLength(Integer length) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import java.io.IOException;
import java.util.Arrays;
import local.m1password.ApiHelper;
import local.m1password.models.CharacterSet;
import local.m1password.models.GeneratorRecipe;

GeneratorRecipe generatorRecipe = new GeneratorRecipe.Builder()
    .characterSets(Arrays.asList(
        CharacterSet.LETTERS,
        CharacterSet.DIGITS,
        CharacterSet.SYMBOLS
    ))
    .excludeCharacters("abc1")
    .length(32)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



