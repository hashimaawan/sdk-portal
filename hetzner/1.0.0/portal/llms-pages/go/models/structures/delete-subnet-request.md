# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | IP range of subnet to delete |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    deleteSubnetRequest := models.DeleteSubnetRequest{
        IpRange:               "10.0.1.0/24",
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



