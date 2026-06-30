# Change IP Range Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNoYW5nZUlQUmFuZ2VSZXF1ZXN0


# Class Name

`ChangeIPRangeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `IpRange` | `string` | Required | The new prefix for the whole Network |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    changeIPRangeRequest := models.ChangeIPRangeRequest{
        IpRange:              "10.0.0.0/12",
    }

}
```



