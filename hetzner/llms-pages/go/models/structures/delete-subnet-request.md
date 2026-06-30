# Delete Subnet Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkRlbGV0ZVN1Ym5ldFJlcXVlc3Q


# Class Name

`DeleteSubnetRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | IP range of subnet to delete |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    deleteSubnetRequest := models.DeleteSubnetRequest{
        IpRange:              "10.0.1.0/24",
    }

}
```



