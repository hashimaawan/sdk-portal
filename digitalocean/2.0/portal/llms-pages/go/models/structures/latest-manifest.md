# Latest Manifest

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkxhdGVzdE1hbmlmZXN0

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`LatestManifest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blobs` | [`[]models.Blob`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/blob.md) | Optional | All blobs associated with this manifest |
| `CompressedSizeBytes` | `*int` | Optional | The compressed size of the manifest in bytes. |
| `Digest` | `*string` | Optional | The manifest digest |
| `RegistryName` | `*string` | Optional | The name of the container registry. |
| `Repository` | `*string` | Optional | The name of the repository. |
| `SizeBytes` | `*int` | Optional | The uncompressed size of the manifest in bytes (this size is calculated asynchronously so it may not be immediately available). |
| `Tags` | `[]string` | Optional | All tags associated with this manifest |
| `UpdatedAt` | `*time.Time` | Optional | The time the manifest was last updated. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "log"
    "time"
    "digitalOceanApi/models"
)

func main() {
    parseTime := func(layout, value string, errCallback func(error)) time.Time {
        dateTime, err := time.Parse(layout, value)
        if err != nil {
            errCallback(err) 
       }
        return dateTime
    }
    latestManifest := models.LatestManifest{
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
        },
        CompressedSizeBytes:   models.ToPointer(2803255),
        Digest:                models.ToPointer("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221"),
        RegistryName:          models.ToPointer("example"),
        Repository:            models.ToPointer("repo-1"),
        SizeBytes:             models.ToPointer(5861888),
        Tags:                  []string{
            "latest",
            "v1",
            "v2",
        },
        UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-04-09T23:54:25Z", func(err error) { log.Fatalln(err) })),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



