# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type object.*


# Class Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CharacterSets` | [`List<CharacterSet>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* |
| `ExcludeCharacters` | `string` | Optional | List of all characters that should be excluded from generated passwords. |
| `Length` | `int?` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;
using System.Collections.Generic;

GeneratorRecipe generatorRecipe = new GeneratorRecipe
{
    CharacterSets = new List<CharacterSet>
    {
        CharacterSet.Letters,
        CharacterSet.Digits,
        CharacterSet.Symbols,
    },
    ExcludeCharacters = "abc1",
    Length = 32,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



