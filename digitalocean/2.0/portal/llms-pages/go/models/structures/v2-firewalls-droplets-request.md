# V2 Firewalls Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBGaXJld2FsbHMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2FirewallsDropletsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletIds` | `[]int` | Required | An array containing the IDs of the Droplets to be removed from the firewall. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2FirewallsDropletsRequest := models.V2FirewallsDropletsRequest{
        DropletIds:            []int{
            49696269,
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



