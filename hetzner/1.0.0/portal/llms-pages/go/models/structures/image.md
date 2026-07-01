# Image

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkltYWdl

*This model accepts additional fields of type interface{}.*


# Class Name

`Image`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BoundTo` | `*int` | Required | ID of Server the Image is bound to. Only set for Images of type `backup`. |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `CreatedFrom` | [`*models.CreatedFrom`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/created-from.md) | Required | Information about the Server the Image was created from |
| `Deleted` | `*string` | Required | Point in time where the Image was deleted (in ISO-8601 format) |
| `Deprecated` | `*string` | Required | Point in time when the Image is considered to be deprecated (in ISO-8601 format) |
| `Description` | `string` | Required | Description of the Image |
| `DiskSize` | `float64` | Required | Size of the disk contained in the Image in GB |
| `Id` | `int` | Required | ID of the Resource |
| `ImageSize` | `*float64` | Required | Size of the Image file in our storage in GB. For snapshot Images this is the value relevant for calculating costs for the Image. |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `Name` | `*string` | Required | Unique identifier of the Image. This value is only set for system Images. |
| `OsFlavor` | [`models.OsFlavor`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/os-flavor.md) | Required | Flavor of operating system contained in the Image |
| `OsVersion` | `*string` | Required | Operating system version |
| `Protection` | [`models.Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `RapidDeploy` | `*bool` | Optional | Indicates that rapid deploy of the Image is available |
| `Status` | [`models.Status24`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-24.md) | Required | Whether the Image can be used or if it's still being created or unavailable |
| `Type` | [`models.Type22`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-22.md) | Required | Type of the Image |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    image := models.Image{
        BoundTo:               nil,
        Created:               "2016-01-30T23:55:00+00:00",
        CreatedFrom:           models.ToPointer(models.CreatedFrom{
            Id:                    1,
            Name:                  "Server",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Deleted:               nil,
        Deprecated:            models.ToPointer("2018-02-28T00:00:00+00:00"),
        Description:           "Ubuntu 20.04 Standard 64 bit",
        DiskSize:              float64(10),
        Id:                    42,
        ImageSize:             models.ToPointer(float64(2.3)),
        Labels:                map[string]string{
            "key0": "labels4",
        },
        Name:                  models.ToPointer("ubuntu-20.04"),
        OsFlavor:              models.OsFlavor_Ubuntu,
        OsVersion:             models.ToPointer("20.04"),
        Protection:            models.Protection{
            Delete:                false,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        RapidDeploy:           models.ToPointer(false),
        Status:                models.Status24_Unavailable,
        Type:                  models.Type22_Snapshot,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



