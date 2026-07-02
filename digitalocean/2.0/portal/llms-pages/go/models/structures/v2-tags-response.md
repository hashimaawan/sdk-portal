# V2 Tags Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2TagsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tags` | [`[]models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/tag.md) | Optional | - |
| `Links` | [`*models.Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/links.md) | Optional | - |
| `Meta` | [`models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/meta.md) | Required | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2TagsResponse := models.V2TagsResponse{
        Tags:                  []models.Tag{
            models.Tag{
                Name:                  models.ToPointer("extra-awesome"),
                Resources:             models.ToPointer(models.Resources2{
                    Count:                 models.ToPointer(5),
                    LastTaggedUri:         models.ToPointer("https://api.digitalocean.com/v2/images/7555620"),
                    Databases:             models.ToPointer(models.Databases{
                        Count:                 models.ToPointer(1),
                        LastTaggedUri:         models.ToPointer("https://api.digitalocean.com/v2/databases/b92438f6-ba03-416c-b642-e9236db91976"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Droplets:              models.ToPointer(models.Databases{
                        Count:                 models.ToPointer(1),
                        LastTaggedUri:         models.ToPointer("https://api.digitalocean.com/v2/droplets/3164444"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Imgages:               models.ToPointer(models.Databases{
                        Count:                 models.ToPointer(158),
                        LastTaggedUri:         models.ToPointer("last_tagged_uri4"),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    VolumeSnapshots:       models.ToPointer(models.Databases{
                        Count:                 models.ToPointer(1),
                        LastTaggedUri:         models.ToPointer("https://api.digitalocean.com/v2/snapshots/1f6f46e8-6b60-11e9-be4e-0a58ac144519"),
                    }),
                    Volumes:               models.ToPointer(models.Databases{
                        Count:                 models.ToPointer(1),
                        LastTaggedUri:         models.ToPointer("https://api.digitalocean.com/v2/volumes/3d80cb72-342b-4aaa-b92e-4e4abb24a933"),
                    }),
                    AdditionalProperties:  map[string]interface{}{
                        "images": interface{}("[count, 1][last_tagged_uri, https://api.digitalocean.com/v2/images/7555620]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Links:                 models.ToPointer(models.Links{
            Pages:                 models.ToPointer(models.LinksPagesContainer.FromPages(models.Pages{
                Last:                  models.ToPointer("last6"),
                Next:                  models.ToPointer("next2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Meta:                  models.Meta{
            Total:                 1,
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



