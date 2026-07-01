# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Isos` | [`[]models.Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/iso.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    isosResponse := models.IsosResponse{
        Isos:                 []models.Iso{
            models.Iso{
                Deprecated:           models.ToPointer("2018-02-28T00:00:00+00:00"),
                Description:          "FreeBSD 11.0 x64",
                Id:                   42,
                Name:                 models.ToPointer("FreeBSD-11.0-RELEASE-amd64-dvd1"),
                Type:                 models.Type26Enum_PUBLIC,
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



