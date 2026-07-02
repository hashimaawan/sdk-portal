# V2 Databases Maintenance Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyME1haW50ZW5hbmNlJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DatabasesMaintenanceRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Day` | `string` | Required | The day of the week on which to apply maintenance updates. |
| `Description` | `[]string` | Optional, Read-only | A list of strings, each containing information about a pending maintenance update. |
| `Hour` | `string` | Required | The hour in UTC at which maintenance updates will be applied in 24 hour format. |
| `Pending` | `*bool` | Optional, Read-only | A boolean value indicating whether any maintenance is scheduled to be performed in the next window. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DatabasesMaintenanceRequest := models.V2DatabasesMaintenanceRequest{
        Day:                   "tuesday",
        Description:           []string{
            "Update TimescaleDB to version 1.2.1",
            "Upgrade to PostgreSQL 11.2 and 10.7 bugfix releases",
        },
        Hour:                  "14:00",
        Pending:               models.ToPointer(true),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



