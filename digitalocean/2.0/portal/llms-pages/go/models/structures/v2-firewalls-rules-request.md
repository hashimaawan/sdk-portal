# V2 Firewalls Rules Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMFJ1bGVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FirewallsRulesRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InboundRules` | [`[]models.InboundRule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/inbound-rule.md) | Required | - |
| `OutboundRules` | [`[]models.OutboundRule`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/outbound-rule.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2FirewallsRulesRequest := models.V2FirewallsRulesRequest{
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



