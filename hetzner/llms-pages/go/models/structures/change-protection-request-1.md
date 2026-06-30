# Change Protection Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkNoYW5nZVByb3RlY3Rpb25SZXF1ZXN0MQ


# Class Name

`ChangeProtectionRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `*bool` | Optional | If true, prevents the Network from being deleted |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    changeProtectionRequest1 := models.ChangeProtectionRequest1{
        Delete:               models.ToPointer(true),
    }

}
```



