# Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZVR5cGVSZXF1ZXN0


# Class Name

`ChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancerType` | `string` | Required | ID or name of Load Balancer type the Load Balancer should migrate to |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    changeTypeRequest := models.ChangeTypeRequest{
        LoadBalancerType:     "lb21",
    }

}
```



