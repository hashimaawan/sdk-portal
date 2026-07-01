# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `Image` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/image.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversActionsCreateImageResponse := models.ServersActionsCreateImageResponse{
        Action:                models.ToPointer(models.Action{
            Command:               "command6",
            Error:                 models.ToPointer(models.Error{
                Code:                  "code2",
                Message:               "message4",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Finished:              models.ToPointer("finished0"),
            Id:                    238,
            Progress:              float64(143.26),
            Resources:             []models.Resource{
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Resource{
                    Id:                    198,
                    Type:                  "type0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Started:               "started8",
            Status:                models.Status_Running,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Image:                 models.ToPointer(models.Image{
            BoundTo:               models.ToPointer(186),
            Created:               "created6",
            CreatedFrom:           models.ToPointer(models.CreatedFrom{
                Id:                    60,
                Name:                  "name6",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Deleted:               models.ToPointer("deleted4"),
            Deprecated:            models.ToPointer("deprecated8"),
            Description:           "description6",
            DiskSize:              float64(244.18),
            Id:                    128,
            ImageSize:             models.ToPointer(float64(141.34)),
            Labels:                map[string]string{
                "key0": "labels4",
            },
            Name:                  models.ToPointer("name6"),
            OsFlavor:              models.OsFlavor_Debian,
            OsVersion:             models.ToPointer("os_version4"),
            Protection:            models.Protection{
                Delete:                false,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            RapidDeploy:           models.ToPointer(false),
            Status:                models.Status24_Unavailable,
            Type:                  models.Type22_App,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



