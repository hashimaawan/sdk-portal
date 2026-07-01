# Volumes Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMFJlc3BvbnNlMg


# Class Name

`VolumesResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Volume` | [`models.Volume1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/volume-1.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    volumesResponse2 := models.VolumesResponse2{
        Volume:               models.Volume1{
            Created:              "2016-01-30T23:55:00+00:00",
            Format:               models.ToPointer("xfs"),
            Id:                   42,
            Labels:               map[string]string{
                "key0": "labels8",
                "key1": "labels9",
                "key2": "labels0",
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
        },
    }

}
```



