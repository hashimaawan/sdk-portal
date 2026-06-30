# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/action.md) | Optional | - |
| `Image` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/image.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    serversActionsCreateImageResponse := models.ServersActionsCreateImageResponse{
        Action:               models.ToPointer(models.Action{
            Command:              "command6",
            Error:                models.ToPointer(models.Error{
                Code:                 "code2",
                Message:              "message4",
            }),
            Finished:             models.ToPointer("finished0"),
            Id:                   238,
            Progress:             float64(143.26),
            Resources:            []models.Resource{
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
            },
            Started:              "started8",
            Status:               models.StatusEnum_RUNNING,
        }),
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



