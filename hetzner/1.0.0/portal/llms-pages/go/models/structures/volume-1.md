# Volume 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZTE


# Class Name

`Volume1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Format` | `*string` | Required | Filesystem of the Volume if formatted on creation, null if not formatted on creation |
| `Id` | `int` | Required | ID of the Resource |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `LinuxDevice` | `string` | Required | Device path on the file system for the Volume |
| `Location` | [`models.Location16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/location-16.md) | Required | Location of the Volume. Volume can only be attached to Servers in the same Location. |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`models.Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Server` | `*int` | Required | ID of the Server the Volume is attached to, null if it is not attached at all |
| `Size` | `float64` | Required | Size in GB of the Volume |
| `Status` | [`models.Status113Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-113.md) | Required | Current status of the Volume |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    volume1 := models.Volume1{
        Created:              "2016-01-30T23:55:00+00:00",
        Format:               models.ToPointer("xfs"),
        Id:                   42,
        Labels:               map[string]string{
            "key0": "labels8",
        },
        LinuxDevice:          "/dev/disk/by-id/scsi-0HC_Volume_4711",
        Location:             models.Location16{
            City:                 "Falkenstein",
            Country:              "DE",
            Description:          "Falkenstein DC Park 1",
            Id:                   float64(1),
            Latitude:             float64(50.47612),
            Longitude:            float64(12.370071),
            Name:                 "fsn1",
            NetworkZone:          "eu-central",
        },
        Name:                 "my-resource",
        Protection:           models.Protection{
            Delete:               false,
        },
        Server:               models.ToPointer(12),
        Size:                 float64(42),
        Status:               models.Status113Enum_AVAILABLE,
    }

}
```



