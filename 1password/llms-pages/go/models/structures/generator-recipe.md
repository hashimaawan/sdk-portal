# Generator Recipe

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkdlbmVyYXRvclJlY2lwZQ

The recipe is used in conjunction with the "generate" property to set the character set used to generate a new secure value

*This model accepts additional fields of type interface{}.*


# Class Name

`GeneratorRecipe`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CharacterSets` | [`[]models.CharacterSet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/character-set.md) | Optional | **Constraints**: *Unique Items Required* |
| `ExcludeCharacters` | `*string` | Optional | List of all characters that should be excluded from generated passwords. |
| `Length` | `*int` | Optional | Length of the generated value<br><br>**Default**: `32`<br><br>**Constraints**: `>= 1`, `<= 64` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "m1PasswordConnect/models"
)

func main() {
    generatorRecipe := models.GeneratorRecipe{
        CharacterSets:         []models.CharacterSet{
            models.CharacterSet_Letters,
            models.CharacterSet_Digits,
            models.CharacterSet_Symbols,
        },
        ExcludeCharacters:     models.ToPointer("abc1"),
        Length:                models.ToPointer(32),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



