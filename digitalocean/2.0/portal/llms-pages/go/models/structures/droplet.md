# Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkRyb3BsZXQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`Droplet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BackupIds` | `[]int` | Required | An array of backup IDs of any backups that have been taken of the Droplet instance.  Droplet backups are enabled at the time of the instance creation. |
| `CreatedAt` | `time.Time` | Required | A time value given in ISO8601 combined date and time format that represents when the Droplet was created. |
| `Disk` | `int` | Required | The size of the Droplet's disk in gigabytes. |
| `Features` | `[]string` | Required | An array of features enabled on this Droplet. |
| `Id` | `int` | Required | A unique identifier for each Droplet instance. This is automatically generated upon Droplet creation. |
| `Image` | [`models.Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/image-1.md) | Required | - |
| `Kernel` | [`models.Optional[models.Kernel]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/kernel.md) | Optional | **Note**: All Droplets created after March 2017 use internal kernels by default.<br>These Droplets will have this attribute set to `null`.<br><br>The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)<br>for Droplets with externally managed kernels. This will initially be set to<br>the kernel of the base image when the Droplet is created. |
| `Locked` | `bool` | Required | A boolean value indicating whether the Droplet has been locked, preventing actions by users. |
| `Memory` | `int` | Required | Memory of the Droplet in megabytes.<br><br>**Constraints**: *Multiple Of*: `8` |
| `Name` | `string` | Required | The human-readable name set for the Droplet instance. |
| `Networks` | [`models.Networks`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/networks.md) | Required | The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is. |
| `NextBackupWindow` | [`*models.NextBackupWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/next-backup-window.md) | Required | The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start. |
| `Region` | [`models.Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/region.md) | Required | - |
| `Size` | [`models.Size`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/size.md) | Required | - |
| `SizeSlug` | `string` | Required | The unique slug identifier for the size of this Droplet. |
| `SnapshotIds` | `[]int` | Required | An array of snapshot IDs of any snapshots created from the Droplet instance. |
| `Status` | [`models.Status8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/status-8.md) | Required | A status string indicating the state of the Droplet instance. This may be "new", "active", "off", or "archive". |
| `Tags` | `[]string` | Required | An array of Tags the Droplet has been tagged with. |
| `Vcpus` | `int` | Required | The number of virtual CPUs. |
| `VolumeIds` | `[]string` | Required | A flat array including the unique identifier for each Block Storage volume attached to the Droplet. |
| `VpcUuid` | `*string` | Optional | A string specifying the UUID of the VPC to which the Droplet is assigned. |
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
    droplet := models.Droplet{
        BackupIds:             []int{
            53893572,
        },
        CreatedAt:             parseTime(time.RFC3339, "2020-07-21T18:37:44Z", func(err error) { log.Fatalln(err) }),
        Disk:                  25,
        Features:              []string{
            "backups",
            "private_networking",
            "ipv6",
        },
        Id:                    3164444,
        Image:                 models.Image1{
            CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2020-05-04T22:23:02Z", func(err error) { log.Fatalln(err) })),
            Description:           models.ToPointer("description6"),
            Distribution:          models.ToPointer(models.Distribution_Ubuntu),
            ErrorMessage:          models.ToPointer("error_message8"),
            Id:                    models.ToPointer(7555620),
            MinDiskSize:           models.NewOptional(models.ToPointer(20)),
            Name:                  models.ToPointer("Nifty New Snapshot"),
            Public:                models.ToPointer(true),
            Regions:               []models.Region2{
                models.Region2_Nyc1,
                models.Region2_Nyc2,
            },
            SizeGigabytes:         models.NewOptional(models.ToPointer(float64(2.34))),
            Slug:                  models.NewOptional(models.ToPointer("nifty1")),
            Status:                models.ToPointer(models.Status7_New),
            Tags:                  models.NewOptional(models.ToPointer([]string{
                "base-image",
                "prod",
            })),
            Type:                  models.ToPointer(models.Type9_Snapshot),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Kernel:                models.NewOptional(models.ToPointer(models.Kernel{
            Id:                    models.ToPointer(16),
            Name:                  models.ToPointer("name4"),
            Version:               models.ToPointer("version0"),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        })),
        Locked:                false,
        Memory:                1024,
        Name:                  "example.com",
        Networks:              models.Networks{
            V4:                    []models.V4{
                models.V4{
                    Gateway:               models.ToPointer("gateway2"),
                    IpAddress:             models.ToPointer("ip_address2"),
                    Netmask:               models.ToPointer("netmask2"),
                    Type:                  models.ToPointer(models.Type10_Public),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.V4{
                    Gateway:               models.ToPointer("gateway2"),
                    IpAddress:             models.ToPointer("ip_address2"),
                    Netmask:               models.ToPointer("netmask2"),
                    Type:                  models.ToPointer(models.Type10_Public),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.V4{
                    Gateway:               models.ToPointer("gateway2"),
                    IpAddress:             models.ToPointer("ip_address2"),
                    Netmask:               models.ToPointer("netmask2"),
                    Type:                  models.ToPointer(models.Type10_Public),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            V6:                    []models.V6{
                models.V6{
                    Gateway:               models.ToPointer("gateway4"),
                    IpAddress:             models.ToPointer("ip_address4"),
                    Netmask:               models.ToPointer(106),
                    Type:                  models.ToPointer(models.Type11_Public),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.V6{
                    Gateway:               models.ToPointer("gateway4"),
                    IpAddress:             models.ToPointer("ip_address4"),
                    Netmask:               models.ToPointer(106),
                    Type:                  models.ToPointer(models.Type11_Public),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        NextBackupWindow:      models.ToPointer(models.NextBackupWindow{
            End:                   models.ToPointer(parseTime(time.RFC3339, "2019-12-04T23:00:00Z", func(err error) { log.Fatalln(err) })),
            Start:                 models.ToPointer(parseTime(time.RFC3339, "2019-12-04T00:00:00Z", func(err error) { log.Fatalln(err) })),
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Region:                models.Region{
            Available:             true,
            Features:              []string{
                "private_networking",
                "backups",
                "ipv6",
                "metadata",
                "install_agent",
                "storage",
                "image_transfer",
            },
            Name:                  "New York 3",
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
                "s-32vcpu-192g",
            },
            Slug:                  "nyc3",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Size:                  models.Size{
            Available:             true,
            Description:           "Basic",
            Disk:                  25,
            Memory:                1024,
            PriceHourly:           float64(0.00743999984115362),
            PriceMonthly:          float64(5),
            Regions:               []string{
                "ams2",
                "ams3",
                "blr1",
                "fra1",
                "lon1",
                "nyc1",
                "nyc2",
                "nyc3",
                "sfo1",
                "sfo2",
                "sfo3",
                "sgp1",
                "tor1",
            },
            Slug:                  "s-1vcpu-1gb",
            Transfer:              float64(1),
            Vcpus:                 1,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        SizeSlug:              "s-1vcpu-1gb",
        SnapshotIds:           []int{
            67512819,
        },
        Status:                models.Status8_Active,
        Tags:                  []string{
            "web",
            "env:prod",
        },
        Vcpus:                 1,
        VolumeIds:             []string{
            "506f78a4-e098-11e5-ad9f-000f53306ae1",
        },
        VpcUuid:               models.ToPointer("760e09ef-dc84-11e8-981e-3cfdfeaae000"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



