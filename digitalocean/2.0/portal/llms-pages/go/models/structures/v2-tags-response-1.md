# V2 Tags Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBUYWdzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2TagsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Tag` | [`*models.Tag`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/tag.md) | Optional | A tag is a label that can be applied to a resource (currently Droplets, Images, Volumes, Volume Snapshots, and Database clusters) in order to better organize or facilitate the lookups and actions on it.<br>Tags have two attributes: a user defined `name` attribute and an embedded `resources` attribute with information about resources that have been tagged. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2TagsResponse1 := models.V2TagsResponse1{
        Tag:                   models.ToPointer(models.Tag{
            Name:                  models.ToPointer("extra-awesome"),
            Resources:             models.ToPointer(models.Resources2{
                Count:                 models.ToPointer(0),
                LastTaggedUri:         models.ToPointer("last_tagged_uri6"),
                Databases:             models.ToPointer(models.Databases{
                    Count:                 models.ToPointer(0),
                    LastTaggedUri:         models.ToPointer("last_tagged_uri2"),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Droplets:              models.ToPointer(models.Databases{
                    Count:                 models.ToPointer(0),
                    LastTaggedUri:         models.ToPointer("last_tagged_uri6"),
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
                    Count:                 models.ToPointer(0),
                }),
                Volumes:               models.ToPointer(models.Databases{
                    Count:                 models.ToPointer(0),
                }),
                AdditionalProperties:  map[string]interface{}{
                    "images": interface{}("[count, 0]"),
                },
            }),
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



