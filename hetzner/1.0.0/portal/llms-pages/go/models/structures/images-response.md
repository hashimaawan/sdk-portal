# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Images` | [`[]models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/image.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    imagesResponse := models.ImagesResponse{
        Images:               []models.Image{
            models.Image{
                BoundTo:              nil,
                Created:              "2016-01-30T23:55:00+00:00",
                CreatedFrom:          models.ToPointer(models.CreatedFrom{
                    Id:                   1,
                    Name:                 "Server",
                }),
                Deleted:              nil,
                Deprecated:           models.ToPointer("2018-02-28T00:00:00+00:00"),
                Description:          "Ubuntu 20.04 Standard 64 bit",
                DiskSize:             float64(10),
                Id:                   42,
                ImageSize:            models.ToPointer(float64(2.3)),
                Labels:               map[string]string{
                    "key0": "labels0",
                    "key1": "labels1",
                },
                Name:                 models.ToPointer("ubuntu-20.04"),
                OsFlavor:             models.OsFlavorEnum_UBUNTU,
                OsVersion:            models.ToPointer("20.04"),
                Protection:           models.Protection{
                    Delete:               false,
                },
                RapidDeploy:          models.ToPointer(false),
                Status:               models.Status24Enum_AVAILABLE,
                Type:                 models.Type22Enum_SNAPSHOT,
            },
        },
        Meta:                 models.ToPointer(models.Meta{
            Pagination:           models.Pagination{
                LastPage:             models.ToPointer(float64(77.7)),
                NextPage:             models.ToPointer(float64(209.18)),
                Page:                 float64(17.58),
                PerPage:              float64(13.34),
                PreviousPage:         models.ToPointer(float64(50.02)),
                TotalEntries:         models.ToPointer(float64(206.64)),
            },
        }),
    }

}
```



