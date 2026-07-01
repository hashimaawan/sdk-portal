# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `*bool` | Optional | Auto-mount Volume after attach. `server` must be provided. |
| `Format` | `*string` | Optional | Format Volume after creation. One of: `xfs`, `ext4` |
| `Labels` | `*interface{}` | Optional | User-defined labels (key-value pairs) |
| `Location` | `*string` | Optional | Location to create the Volume in (can be omitted if Server is specified) |
| `Name` | `string` | Required | Name of the volume |
| `Server` | `*int` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) |
| `Size` | `int` | Required | Size of the Volume in GB |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createVolumeRequest := models.CreateVolumeRequest{
        Automount:            models.ToPointer(false),
        Format:               models.ToPointer("xfs"),
        Labels:               models.ToPointer(interface{}("[labelkey, value]")),
        Location:             models.ToPointer("nbg1"),
        Name:                 "databases-storage",
        Server:               models.ToPointer(182),
        Size:                 42,
    }

}
```



