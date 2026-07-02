# Inbound Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkluYm91bmRSdWxl

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`InboundRule`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Ports` | `string` | Required | The ports on which traffic will be allowed specified as a string containing a single port, a range (e.g. "8000-9000"), or "0" when all ports are open for a protocol. For ICMP rules this parameter will always return "0". |
| `Protocol` | [`models.Protocol`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/protocol.md) | Required | The type of traffic to be allowed. This may be one of `tcp`, `udp`, or `icmp`. |
| `Sources` | [`models.Sources`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/sources.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    inboundRule := models.InboundRule{
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
    }

}
```



