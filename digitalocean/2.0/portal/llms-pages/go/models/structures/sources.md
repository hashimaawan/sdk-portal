# Sources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlNvdXJjZXM

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Sources`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Addresses` | `[]string` | Optional | An array of strings containing the IPv4 addresses, IPv6 addresses, IPv4 CIDRs, and/or IPv6 CIDRs to which the firewall will allow traffic. |
| `DropletIds` | `[]int` | Optional | An array containing the IDs of the Droplets to which the firewall will allow traffic. |
| `KubernetesIds` | `[]string` | Optional | An array containing the IDs of the Kubernetes clusters to which the firewall will allow traffic. |
| `LoadBalancerUids` | `[]string` | Optional | An array containing the IDs of the load balancers to which the firewall will allow traffic. |
| `Tags` | `models.Optional[[]string]` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    sources := models.Sources{
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
    }

}
```



