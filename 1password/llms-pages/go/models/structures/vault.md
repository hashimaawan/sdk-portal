# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/go/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type interface{}.*


# Class Name

`Vault`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AttributeVersion` | `*int` | Optional | The vault version |
| `ContentVersion` | `*int` | Optional | The version of the vault contents |
| `CreatedAt` | `*time.Time` | Optional, Read-only | - |
| `Description` | `*string` | Optional | - |
| `Id` | `*string` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `Items` | `*int` | Optional | Number of active items in the vault |
| `Name` | `*string` | Optional | - |
| `Type` | [`*models.Type2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/go/models/enumerations/type-2.md) | Optional | - |
| `UpdatedAt` | `*time.Time` | Optional, Read-only | - |
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
    vault := models.Vault{
        AttributeVersion:      models.ToPointer(108),
        ContentVersion:        models.ToPointer(228),
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
        Description:           models.ToPointer("description6"),
        Id:                    models.ToPointer("id6"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



