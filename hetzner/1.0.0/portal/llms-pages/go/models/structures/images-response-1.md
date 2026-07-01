# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    imagesResponse1 := models.ImagesResponse1{
        Image:                models.ToPointer(models.Image{
            BoundTo:              models.ToPointer(186),
            Created:              "created6",
            CreatedFrom:          models.ToPointer(models.CreatedFrom{
                Id:                   60,
                Name:                 "name6",
            }),
            Deleted:              models.ToPointer("deleted4"),
            Deprecated:           models.ToPointer("deprecated8"),
            Description:          "description6",
            DiskSize:             float64(244.18),
            Id:                   128,
            ImageSize:            models.ToPointer(float64(141.34)),
            Labels:               map[string]string{
                "key0": "labels4",
            },
            Name:                 models.ToPointer("name6"),
            OsFlavor:             models.OsFlavorEnum_DEBIAN,
            OsVersion:            models.ToPointer("os_version4"),
            Protection:           models.Protection{
                Delete:               false,
            },
            RapidDeploy:          models.ToPointer(false),
            Status:               models.Status24Enum_UNAVAILABLE,
            Type:                 models.Type22Enum_APP,
        }),
    }

}
```



