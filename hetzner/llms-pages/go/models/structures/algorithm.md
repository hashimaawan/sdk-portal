# Algorithm

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkFsZ29yaXRobQ

Algorithm of the Load Balancer


# Class Name

`Algorithm`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Type` | [`models.Type28Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-28.md) | Required | Type of the algorithm |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    algorithm := models.Algorithm{
        Type:                 models.Type28Enum_ROUNDROBIN,
    }

}
```



