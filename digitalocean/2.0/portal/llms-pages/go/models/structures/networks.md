# Networks

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRk5ldHdvcmtz

The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Networks`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `V4` | [`[]models.V4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v4.md) | Optional | - |
| `V6` | [`[]models.V6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/v6.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    networks := models.Networks{
        V4:                    []models.V4{
            models.V4{
                Gateway:               models.ToPointer("gateway2"),
                IpAddress:             models.ToPointer("ip_address2"),
                Netmask:               models.ToPointer("netmask2"),
                Type:                  models.ToPointer(models.Type10_Public),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.V4{
                Gateway:               models.ToPointer("gateway2"),
                IpAddress:             models.ToPointer("ip_address2"),
                Netmask:               models.ToPointer("netmask2"),
                Type:                  models.ToPointer(models.Type10_Public),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.V4{
                Gateway:               models.ToPointer("gateway2"),
                IpAddress:             models.ToPointer("ip_address2"),
                Netmask:               models.ToPointer("netmask2"),
                Type:                  models.ToPointer(models.Type10_Public),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        V6:                    []models.V6{
            models.V6{
                Gateway:               models.ToPointer("gateway4"),
                IpAddress:             models.ToPointer("ip_address4"),
                Netmask:               models.ToPointer(106),
                Type:                  models.ToPointer(models.Type11_Public),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.V6{
                Gateway:               models.ToPointer("gateway4"),
                IpAddress:             models.ToPointer("ip_address4"),
                Netmask:               models.ToPointer(106),
                Type:                  models.ToPointer(models.Type11_Public),
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



