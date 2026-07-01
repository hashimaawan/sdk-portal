# Create Firewall Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVxdWVzdA

*This model accepts additional fields of type interface{}.*


# Class Name

`CreateFirewallRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ApplyTo` | [`[]models.ApplyTo`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/apply-to.md) | Optional | Resources the Firewall should be applied to after creation |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Firewall |
| `Rules` | [`[]models.Rule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/rule.md) | Optional | Array of rules |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    createFirewallRequest := models.CreateFirewallRequest{
        ApplyTo:               []models.ApplyTo{
            models.ApplyTo{
                LabelSelector:         models.ToPointer(models.LabelSelector1{
                    Selector:              "selector8",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Server:                models.ToPointer(models.Server2{
                    Id:                    14,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  models.Type7_Server,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.ApplyTo{
                LabelSelector:         models.ToPointer(models.LabelSelector1{
                    Selector:              "selector8",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Server:                models.ToPointer(models.Server2{
                    Id:                    14,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  models.Type7_Server,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.ApplyTo{
                LabelSelector:         models.ToPointer(models.LabelSelector1{
                    Selector:              "selector8",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Server:                models.ToPointer(models.Server2{
                    Id:                    14,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Type:                  models.Type7_Server,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Labels:                models.ToPointer(interface{}("[key1, val1][key2, val2]")),
        Name:                  "Corporate Intranet Protection",
        Rules:                 []models.Rule{
            models.Rule{
                Description:           models.NewOptional(models.ToPointer("description2")),
                DestinationIps:        []string{
                    "destination_ips1",
                    "destination_ips2",
                    "destination_ips3",
                },
                Direction:             models.Direction_In,
                Port:                  models.ToPointer("80"),
                Protocol:              models.Protocol_Tcp,
                SourceIps:             []string{
                    "28.239.13.1/32",
                    "28.239.14.0/24",
                    "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
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



