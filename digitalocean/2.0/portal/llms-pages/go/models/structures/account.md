# Account

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkFjY291bnQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Account`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletLimit` | `int` | Required | The total number of Droplets current user or team may have active at one time. |
| `Email` | `string` | Required | The email address used by the current user to register for DigitalOcean. |
| `EmailVerified` | `bool` | Required | If true, the user has verified their account via email. False otherwise.<br><br>**Default**: `false` |
| `FloatingIpLimit` | `int` | Required | The total number of Floating IPs the current user or team may have. |
| `Status` | [`models.Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status.md) | Required | This value is one of "active", "warning" or "locked".<br><br>**Default**: `"active"` |
| `StatusMessage` | `string` | Required | A human-readable message giving more details about the status of the account. |
| `Team` | [`*models.Team`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/team.md) | Optional | When authorized in a team context, includes information about the current team. |
| `Uuid` | `string` | Required | The unique universal identifier for the current user. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    account := models.Account{
        DropletLimit:          25,
        Email:                 "sammy@digitalocean.com",
        EmailVerified:         true,
        FloatingIpLimit:       5,
        Status:                models.Status_Active,
        StatusMessage:         " ",
        Team:                  models.ToPointer(models.Team{
            Name:                  models.ToPointer("name0"),
            Uuid:                  models.ToPointer("uuid6"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Uuid:                  "b6fr89dbf6d9156cace5f3c78dc9851d957381ef",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



