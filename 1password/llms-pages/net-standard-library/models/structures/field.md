# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type object.*


# Class Name

`Field`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Entropy` | `double?` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value |
| `Generate` | `bool?` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `false` |
| `Id` | `string` | Required | - |
| `Label` | `string` | Optional | - |
| `Purpose` | [`Purpose?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. |
| `Recipe` | [`GeneratorRecipe`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value |
| `Section` | [`Section`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/structures/section.md) | Optional | - |
| `Type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/type-1.md) | Required | **Default**: `Type1.STRING` |
| `MValue` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;
using System.Collections.Generic;

Field field = new Field
{
    Id = "id6",
    Type = Type1.MString,
    Entropy = 80.94,
    Generate = false,
    Label = "label6",
    Purpose = Purpose.Notes,
    Recipe = new GeneratorRecipe
    {
        CharacterSets = new List<CharacterSet>
        {
            CharacterSet.Letters,
            CharacterSet.Symbols,
            CharacterSet.Digits,
        },
        ExcludeCharacters = "excludeCharacters0",
        Length = 64,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



