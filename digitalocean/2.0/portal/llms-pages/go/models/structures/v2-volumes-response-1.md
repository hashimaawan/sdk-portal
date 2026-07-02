# V2 Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2VolumesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Volume` | [`*models.Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/volume.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2VolumesResponse1 := models.V2VolumesResponse1{
        Volume:                models.ToPointer(models.Volume{
            CreatedAt:             models.ToPointer("2020-03-02T17:00:49Z"),
            Description:           models.ToPointer("Block store for examples"),
            DropletIds:            models.NewOptional(models.ToPointer([]int{
            })),
            Id:                    models.ToPointer("506f78a4-e098-11e5-ad9f-000f53306ae1"),
            Name:                  models.ToPointer("example"),
            SizeGigabytes:         models.ToPointer(10),
            FilesystemLabel:       models.ToPointer("example"),
            FilesystemType:        models.ToPointer("ext4"),
            Region:                models.ToPointer(models.Region{
                Available:             true,
                Features:              []string{
                    "private_networking",
                    "backups",
                    "ipv6",
                    "metadata",
                },
                Name:                  "New York 1",
                Sizes:                 []string{
                    "s-1vcpu-1gb",
                    "s-1vcpu-2gb",
                    "s-1vcpu-3gb",
                    "s-2vcpu-2gb",
                    "s-3vcpu-1gb",
                    "s-2vcpu-4gb",
                    "s-4vcpu-8gb",
                    "s-6vcpu-16gb",
                    "s-8vcpu-32gb",
                    "s-12vcpu-48gb",
                    "s-16vcpu-64gb",
                    "s-20vcpu-96gb",
                    "s-24vcpu-128gb",
                    "s-32vcpu-192gb",
                },
                Slug:                  "nyc1",
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



