# V2 Load Balancers Droplets Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBMb2FkJTI1MjBCYWxhbmNlcnMlMjUyMERyb3BsZXRzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2LoadBalancersDropletsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DropletIds` | `[]int` | Optional | An array containing the IDs of the Droplets assigned to the load balancer. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2LoadBalancersDropletsRequest := models.V2LoadBalancersDropletsRequest{
        DropletIds:            []int{
            3164444,
            3164445,
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



