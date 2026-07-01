# Error 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkVycm9yMg

If issuance or renewal reports `failed`, this property contains information about what happened


# Class Name

`Error2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Code` | `*string` | Optional | - |
| `Message` | `*string` | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    error2 := models.Error2{
        Code:                 models.ToPointer("code2"),
        Message:              models.ToPointer("message4"),
    }

}
```



