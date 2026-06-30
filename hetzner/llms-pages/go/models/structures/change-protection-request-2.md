# Change Protection Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0Mg


# Class Name

`ChangeProtectionRequest2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the Primary IP from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    changeProtectionRequest2 := models.ChangeProtectionRequest2{
        Delete:               models.ToPointer(true),
    }

}
```



