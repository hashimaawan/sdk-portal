# Repository 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlcG9zaXRvcnkx

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Repository1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LatestManifest` | [`*models.LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/latest-manifest.md) | Optional | - |
| `ManifestCount` | `*int` | Optional | The number of manifests in the repository. |
| `Name` | `*string` | Optional | The name of the repository. |
| `RegistryName` | `*string` | Optional | The name of the container registry. |
| `TagCount` | `*int` | Optional | The number of tags in the repository. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    repository1 := models.Repository1{
        LatestManifest:        models.ToPointer(models.LatestManifest{
            Blobs:                 []models.Blob{
                models.Blob{
                    CompressedSizeBytes:   models.ToPointer(12),
                    Digest:                models.ToPointer("digest2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Blob{
                    CompressedSizeBytes:   models.ToPointer(12),
                    Digest:                models.ToPointer("digest2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.Blob{
                    CompressedSizeBytes:   models.ToPointer(12),
                    Digest:                models.ToPointer("digest2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            CompressedSizeBytes:   models.ToPointer(154),
            Digest:                models.ToPointer("digest0"),
            RegistryName:          models.ToPointer("registry_name4"),
            Repository:            models.ToPointer("repository4"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        ManifestCount:         models.ToPointer(1),
        Name:                  models.ToPointer("repo-1"),
        RegistryName:          models.ToPointer("example"),
        TagCount:              models.ToPointer(1),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



