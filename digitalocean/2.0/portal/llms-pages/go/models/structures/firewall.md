# Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxs

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Firewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. |
| `DropletIds` | `models.Optional[[]int]` | Optional | An array containing the IDs of the Droplets assigned to the firewall. |
| `Id` | `*string` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. |
| `Name` | `*string` | Optional | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` |
| `PendingChanges` | [`[]models.PendingChange`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. |
| `Status` | [`*models.Status9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". |
| `Tags` | `models.Optional[[]string]` | Optional | - |
| `InboundRules` | [`models.Optional[[]models.InboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/inbound-rule.md) | Optional | - |
| `OutboundRules` | [`models.Optional[[]models.OutboundRule]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/outbound-rule.md) | Optional | - |
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
    firewall := models.Firewall{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-23T21:24:00Z", func(err error) { log.Fatalln(err) })),
        DropletIds:            models.NewOptional(models.ToPointer([]int{
            8043964,
        })),
        Id:                    models.ToPointer("bb4b2611-3d72-467b-8602-280330ecd65c"),
        Name:                  models.ToPointer("firewall"),
        PendingChanges:        []models.PendingChange{
            models.PendingChange{
                DropletId:             models.ToPointer(8043964),
                Removing:              models.ToPointer(false),
                Status:                models.ToPointer("waiting"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Status:                models.ToPointer(models.Status9_Waiting),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



