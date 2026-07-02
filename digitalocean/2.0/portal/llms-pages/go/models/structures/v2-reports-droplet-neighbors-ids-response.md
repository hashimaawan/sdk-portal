# V2 Reports Droplet Neighbors Ids Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBSZXBvcnRzJTI1MjBEcm9wbGV0JTI1MjBOZWlnaGJvcnMlMjUyMElkcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2ReportsDropletNeighborsIdsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NeighborIds` | `[][]int` | Optional | An array of arrays. Each array will contain a set of Droplet IDs for Droplets that share a physical server. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2ReportsDropletNeighborsIdsResponse := models.V2ReportsDropletNeighborsIdsResponse{
        NeighborIds:           [][]int{
            []int{
                168671828,
                168663509,
                168671815,
            },
            []int{
                168671883,
                168671750,
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



