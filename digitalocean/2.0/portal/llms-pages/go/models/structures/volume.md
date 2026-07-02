# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CreatedAt` | `*string` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. |
| `Description` | `*string` | Optional | An optional free-form text field to describe a block storage volume. |
| `DropletIds` | `models.Optional[[]int]` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. |
| `Id` | `*string` | Optional, Read-only | The unique identifier for the block storage volume. |
| `Name` | `*string` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. |
| `SizeGigabytes` | `*int` | Optional | The size of the block storage volume in GiB (1024^3). |
| `Tags` | `models.Optional[[]string]` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. |
| `FilesystemLabel` | `*string` | Optional | The label currently applied to the filesystem. |
| `FilesystemType` | `*string` | Optional | The type of filesystem currently in-use on the volume. |
| `Region` | [`*models.Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/region.md) | Optional, Read-only | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    volume := models.Volume{
        CreatedAt:             models.ToPointer("2020-03-02T17:00:49Z"),
        Description:           models.ToPointer("Block store for examples"),
        DropletIds:            models.NewOptional(models.ToPointer([]int{
        })),
        Id:                    models.ToPointer("506f78a4-e098-11e5-ad9f-000f53306ae1"),
        Name:                  models.ToPointer("example"),
        SizeGigabytes:         models.ToPointer(10),
        Tags:                  models.NewOptional(models.ToPointer([]string{
            "base-image",
            "prod",
        })),
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
    }

}
```



