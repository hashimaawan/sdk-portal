# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`[]models.ApplyTo`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Firewall |
| `Rules` | [`[]models.Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/rule.md) | Optional | Array of rules |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createFirewallRequest := models.CreateFirewallRequest{
        ApplyTo:              []models.ApplyTo{
            models.ApplyTo{
                LabelSelector:        models.ToPointer(models.LabelSelector1{
                    Selector:             "selector8",
                }),
                Server:               models.ToPointer(models.Server2{
                    Id:                   14,
                }),
                Type:                 models.Type7Enum_SERVER,
            },
            models.ApplyTo{
                LabelSelector:        models.ToPointer(models.LabelSelector1{
                    Selector:             "selector8",
                }),
                Server:               models.ToPointer(models.Server2{
                    Id:                   14,
                }),
                Type:                 models.Type7Enum_SERVER,
            },
            models.ApplyTo{
                LabelSelector:        models.ToPointer(models.LabelSelector1{
                    Selector:             "selector8",
                }),
                Server:               models.ToPointer(models.Server2{
                    Id:                   14,
                }),
                Type:                 models.Type7Enum_SERVER,
            },
        },
        Labels:               models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Name:                 "Corporate Intranet Protection",
        Rules:                []models.Rule{
            models.Rule{
                Description:          models.NewOptional(models.ToPointer("description2")),
                DestinationIps:       []string{
                    "destination_ips1",
                    "destination_ips2",
                    "destination_ips3",
                },
                Direction:            models.DirectionEnum_IN,
                Port:                 models.ToPointer("80"),
                Protocol:             models.ProtocolEnum_TCP,
                SourceIps:            []string{
                    "28.239.13.1/32",
                    "28.239.14.0/24",
                    "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                },
            },
        },
    }

}
```



