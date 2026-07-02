# V2 Firewalls Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FirewallsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*time.Time` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the firewall was created. |
| `DropletIds` | `models.Optional[[]int]` | Optional | An array containing the IDs of the Droplets assigned to the firewall. |
| `Id` | `*string` | Optional, Read-only | A unique ID that can be used to identify and reference a firewall. |
| `Name` | `string` | Required | A human-readable name for a firewall. The name must begin with an alphanumeric character. Subsequent characters must either be alphanumeric characters, a period (.), or a dash (-).<br><br>**Constraints**: *Pattern*: `^[a-zA-Z0-9][a-zA-Z0-9\.-]+$` |
| `PendingChanges` | [`[]models.PendingChange`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/pending-change.md) | Optional, Read-only | An array of objects each containing the fields "droplet_id", "removing", and "status". It is provided to detail exactly which Droplets are having their security policies updated. When empty, all changes have been successfully applied. |
| `Status` | [`*models.Status9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-9.md) | Optional, Read-only | A status string indicating the current state of the firewall. This can be "waiting", "succeeded", or "failed". |
| `Tags` | `models.Optional[[]string]` | Optional | - |
| `InboundRules` | [`[]models.InboundRule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/inbound-rule.md) | Required | - |
| `OutboundRules` | [`[]models.OutboundRule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/outbound-rule.md) | Required | - |
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
    v2FirewallsRequest := models.V2FirewallsRequest{
        CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-23T21:24:00Z", func(err error) { log.Fatalln(err) })),
        DropletIds:            models.NewOptional(models.ToPointer([]int{
            8043964,
        })),
        Id:                    models.ToPointer("bb4b2611-3d72-467b-8602-280330ecd65c"),
        Name:                  "firewall",
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
        InboundRules:          []models.InboundRule{
            models.InboundRule{
                Ports:                 "8000",
                Protocol:              models.Protocol_Tcp,
                Sources:               models.Sources{
                    Addresses:             []string{
                        "1.2.3.4",
                        "18.0.0.0/8",
                    },
                    DropletIds:            []int{
                        8043964,
                    },
                    KubernetesIds:         []string{
                        "41b74c5d-9bd0-5555-5555-a57c495b81a3",
                    },
                    LoadBalancerUids:      []string{
                        "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                    },
                    Tags:                  models.NewOptional(models.ToPointer([]string{
                        "tags1",
                        "tags2",
                        "tags3",
                    })),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        OutboundRules:         []models.OutboundRule{
            models.OutboundRule{
                Ports:                 "8000",
                Protocol:              models.Protocol_Tcp,
                Destinations:          models.Destinations{
                    Addresses:             []string{
                        "1.2.3.4",
                        "18.0.0.0/8",
                    },
                    DropletIds:            []int{
                        8043964,
                    },
                    KubernetesIds:         []string{
                        "41b74c5d-9bd0-5555-5555-a57c495b81a3",
                    },
                    LoadBalancerUids:      []string{
                        "4de7ac8b-495b-4884-9a69-1050c6793cd6",
                    },
                    Tags:                  models.NewOptional(models.ToPointer([]string{
                        "tags7",
                        "tags8",
                        "tags9",
                    })),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



