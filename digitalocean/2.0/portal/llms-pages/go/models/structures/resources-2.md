# Resources 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlJlc291cmNlczI

An embedded object containing key value pairs of resource type and resource statistics. It also includes a count of the total number of resources tagged with the current tag as well as a `last_tagged_uri` attribute set to the last resource tagged with the current tag.

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Resources2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Count` | `*int` | Optional | The number of tagged objects for this type of resource.<br><br>**Constraints**: `>= 0` |
| `LastTaggedUri` | `*string` | Optional | The URI for the last tagged object for this type of resource. |
| `Databases` | [`*models.Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `Droplets` | [`*models.Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `Imgages` | [`*models.Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `VolumeSnapshots` | [`*models.Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `Volumes` | [`*models.Databases`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/databases.md) | Optional | Tagged Resource Statistics include metadata regarding the resource type that has been tagged. |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    resources2 := models.Resources2{
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
    }

}
```



