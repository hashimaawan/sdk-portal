# Contains All Domains for the App

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkNvbnRhaW5zJTI1MjBhbGwlMjUyMGRvbWFpbnMlMjUyMGZvciUyNTIwdGhlJTI1MjBhcHA

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`ContainsAllDomainsForTheApp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CertificateExpiresAt` | `*time.Time` | Optional, Read-only | - |
| `Id` | `*string` | Optional | - |
| `Phase` | [`*models.Phase1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/phase-1.md) | Optional | **Default**: `"UNKNOWN"` |
| `Progress` | [`*models.Progress1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/progress-1.md) | Optional | - |
| `RotateValidationRecords` | `*bool` | Optional, Read-only | - |
| `Spec` | [`*models.Domain`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/domain.md) | Optional | - |
| `Validations` | [`[]models.ListOfTxtValidationRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/list-of-txt-validation-record.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    containsAllDomainsForTheApp := models.ContainsAllDomainsForTheApp{
        CertificateExpiresAt:    models.ToPointer(parseTime(time.RFC3339, "2024-01-29T23:59:59Z", func(err error) { log.Fatalln(err) })),
        Id:                      models.ToPointer("4f6c71e2-1e90-4762-9fee-6cc4a0a9f2cf"),
        Phase:                   models.ToPointer(models.Phase1_Active),
        Progress:                models.ToPointer(models.Progress1{
            Steps:                 []interface{}{
                interface{}("[key1, val1][key2, val2]"),
                interface{}("[key1, val1][key2, val2]"),
                interface{}("[key1, val1][key2, val2]"),
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        RotateValidationRecords: models.ToPointer(false),
        AdditionalProperties:    map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



