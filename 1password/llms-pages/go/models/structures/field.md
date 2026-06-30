# Field

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkZpZWxk

*This model accepts additional fields of type interface{}.*


# Class Name

`Field`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Entropy` | `*float64` | Optional, Read-only | For fields with a purpose of `PASSWORD` this is the entropy of the value |
| `Generate` | `*bool` | Optional | If value is not present then a new value should be generated for this field<br><br>**Default**: `false` |
| `Id` | `string` | Required | - |
| `Label` | `*string` | Optional | - |
| `Purpose` | [`*models.Purpose`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/purpose.md) | Optional | Some item types, Login and Password, have fields used for autofill. This property indicates that purpose and is required for some item types. |
| `Recipe` | [`*models.GeneratorRecipe`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/generator-recipe.md) | Optional | The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value |
| `Section` | [`*models.Section`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/section.md) | Optional | - |
| `Type` | [`models.Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/type-1.md) | Required | **Default**: `"STRING"` |
| `Value` | `*string` | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    field := models.Field{
        Entropy:               models.ToPointer(float64(80.94)),
        Generate:              models.ToPointer(false),
        Id:                    "id6",
        Label:                 models.ToPointer("label6"),
        Purpose:               models.ToPointer(models.Purpose_Notes),
        Recipe:                models.ToPointer(models.GeneratorRecipe{
            CharacterSets:         []models.CharacterSet{
                models.CharacterSet_Letters,
                models.CharacterSet_Symbols,
                models.CharacterSet_Digits,
            },
            ExcludeCharacters:     models.ToPointer("excludeCharacters0"),
            Length:                models.ToPointer(64),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Type:                  models.Type1_MString,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



