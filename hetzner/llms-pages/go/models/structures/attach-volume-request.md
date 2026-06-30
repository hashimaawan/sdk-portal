# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `*bool` | Optional | Auto-mount the Volume after attaching it |
| `Server` | `int` | Required | ID of the Server the Volume will be attached to |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    attachVolumeRequest := models.AttachVolumeRequest{
        Automount:            models.ToPointer(false),
        Server:               43,
    }

}
```



