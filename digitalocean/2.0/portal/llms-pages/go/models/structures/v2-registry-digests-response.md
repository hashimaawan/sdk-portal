# V2 Registry Digests Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwRGlnZXN0cyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2RegistryDigestsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Manifests` | [`[]models.LatestManifest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/latest-manifest.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
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
    v2RegistryDigestsResponse := models.V2RegistryDigestsResponse{
        Manifests:             []models.LatestManifest{
            models.LatestManifest{
                Blobs:                 []models.Blob{
                    models.Blob{
                        CompressedSizeBytes:   models.ToPointer(1471),
                        Digest:                models.ToPointer("sha256:14119a10abf4669e8cdbdff324a9f9605d99697215a0d21c360fe8dfa8471bab"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    models.Blob{
                        CompressedSizeBytes:   models.ToPointer(12),
                        Digest:                models.ToPointer("sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e"),
                        AdditionalProperties:  map[string]interface{}{
                            "compressed_size_byte": interface{}("2814446"),
                        },
                    },
                    models.Blob{
                        CompressedSizeBytes:   models.ToPointer(528),
                        Digest:                models.ToPointer("sha256:69704ef328d05a9f806b6b8502915e6a0a4faa4d72018dc42343f511490daf8a"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                CompressedSizeBytes:   models.ToPointer(1972332),
                Digest:                models.ToPointer("sha256:cb8a924afdf0229ef7515d9e5b3024e23b3eb03ddbba287f4a19c6ac90b8d221"),
                RegistryName:          models.ToPointer("example"),
                Repository:            models.ToPointer("repo-1"),
                SizeBytes:             models.ToPointer(2816445),
                Tags:                  []string{
                    "v1",
                    "v2",
                },
                UpdatedAt:             models.ToPointer(parseTime(time.RFC3339, "2021-04-09T23:54:25Z", func(err error) { log.Fatalln(err) })),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1"),
                Next:                  models.ToPointer("https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=3&per_page=1"),
                AdditionalProperties:  map[string]interface{}{
                    "first": interface{}("https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1"),
                    "prev": interface{}("https://api.digitalocean.com/v2/registry/example/repositories/repo-1/digests?page=1&per_page=1"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 3,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



