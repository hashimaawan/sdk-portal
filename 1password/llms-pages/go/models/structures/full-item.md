# Full Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRkZ1bGxJdGVt

*This model accepts additional fields of type interface{}.*


# Class Name

`FullItem`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Category` | [`models.Category`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/category.md) | Required | - |
| `CreatedAt` | `*time.Time` | Optional, Read-only | - |
| `Favorite` | `*bool` | Optional | **Default**: `false` |
| `Id` | `*string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `LastEditedBy` | `*string` | Optional, Read-only | - |
| `State` | [`*models.State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/state.md) | Optional, Read-only | - |
| `Tags` | `[]string` | Optional | - |
| `Title` | `*string` | Optional | - |
| `UpdatedAt` | `*time.Time` | Optional, Read-only | - |
| `Urls` | [`[]models.Url`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/url.md) | Optional | - |
| `Vault` | [`models.Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/vault-1.md) | Required | - |
| `Version` | `*int` | Optional | - |
| `Fields` | [`[]models.Field`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/field.md) | Optional | - |
| `Files` | [`[]models.File`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/file.md) | Optional | - |
| `Sections` | [`[]models.Section2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/structures/section-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "m1PasswordConnect/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    fullItem := models.FullItem{
        Category:              models.Category_Membership,
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Favorite:              models.ToPointer(false),
        Id:                    models.ToPointer("id0"),
        LastEditedBy:          models.ToPointer("lastEditedBy6"),
        State:                 models.ToPointer(models.State_Archived),
        Urls:                  []models.Url{
            models.Url{
                Href:                  "https://example.com",
                Primary:               models.ToPointer(true),
            },
            models.Url{
                Href:                  "https://example.org",
            },
        },
        Vault:                 models.Vault1{
            Id:                    "id6",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



