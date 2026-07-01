# Created From

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZWRGcm9t

Information about the Server the Image was created from


# Class Name

`CreatedFrom`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `int` | Required | ID of the Server the Image was created from |
| `Name` | `string` | Required | Server name at the time the Image was created |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createdFrom := models.CreatedFrom{
        Id:                   1,
        Name:                 "Server",
    }

}
```



