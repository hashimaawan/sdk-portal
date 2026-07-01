# Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0


# Class Name

`ChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the Floating IP from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    changeProtectionRequest := models.ChangeProtectionRequest{
        Delete:               models.ToPointer(true),
    }

}
```



