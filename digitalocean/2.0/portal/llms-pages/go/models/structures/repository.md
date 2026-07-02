# Repository

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlcG9zaXRvcnk

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Repository`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LatestTag` | [`*models.LatestTag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/latest-tag.md) | Optional | - |
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
    repository := models.Repository{
        LatestTag:             models.ToPointer(models.LatestTag{
            CompressedSizeBytes:   models.ToPointer(108),
            ManifestDigest:        models.ToPointer("manifest_digest2"),
            RegistryName:          models.ToPointer("registry_name4"),
            Repository:            models.ToPointer("repository4"),
            SizeBytes:             models.ToPointer(226),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Name:                  models.ToPointer("repo-1"),
        RegistryName:          models.ToPointer("example"),
        TagCount:              models.ToPointer(1),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



