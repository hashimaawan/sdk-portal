# V2 Droplets Neighbors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwTmVpZ2hib3JzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DropletsNeighborsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Droplets` | [`[]models.Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/droplet.md) | Optional | - |
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
    v2DropletsNeighborsResponse := models.V2DropletsNeighborsResponse{
        Droplets:              []models.Droplet{
            models.Droplet{
                BackupIds:             []int{
                    104,
                    105,
                },
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                Disk:                  98,
                Features:              []string{
                    "features1",
                    "features2",
                    "features3",
                },
                Id:                    232,
                Image:                 models.Image1{
                    CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    Description:           models.ToPointer("description6"),
                    Distribution:          models.ToPointer(models.Distribution_Coreos),
                    ErrorMessage:          models.ToPointer("error_message8"),
                    Id:                    models.ToPointer(128),
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
                Memory:                16,
                Name:                  "name0",
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
                    End:                   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    Start:                 models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Region:                models.Region{
                    Available:             false,
                    Features:              []string{
                        "features7",
                        "features8",
                        "features9",
                    },
                    Name:                  "name6",
                    Sizes:                 []string{
                        "sizes6",
                    },
                    Slug:                  "slug0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Size:                  models.Size{
                    Available:             false,
                    Description:           "description0",
                    Disk:                  252,
                    Memory:                168,
                    PriceHourly:           float64(121.04),
                    PriceMonthly:          float64(162.04),
                    Regions:               []string{
                        "regions5",
                    },
                    Slug:                  "slug6",
                    Transfer:              float64(150.78),
                    Vcpus:                 234,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                SizeSlug:              "size_slug0",
                SnapshotIds:           []int{
                    93,
                    94,
                },
                Status:                models.Status8_New,
                Tags:                  []string{
                    "tags5",
                },
                Vcpus:                 80,
                VolumeIds:             []string{
                    "volume_ids0",
                    "volume_ids1",
                    "volume_ids2",
                },
                VpcUuid:               models.ToPointer("vpc_uuid0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet{
                BackupIds:             []int{
                    104,
                    105,
                },
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                Disk:                  98,
                Features:              []string{
                    "features1",
                    "features2",
                    "features3",
                },
                Id:                    232,
                Image:                 models.Image1{
                    CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    Description:           models.ToPointer("description6"),
                    Distribution:          models.ToPointer(models.Distribution_Coreos),
                    ErrorMessage:          models.ToPointer("error_message8"),
                    Id:                    models.ToPointer(128),
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
                Memory:                16,
                Name:                  "name0",
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
                    End:                   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    Start:                 models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Region:                models.Region{
                    Available:             false,
                    Features:              []string{
                        "features7",
                        "features8",
                        "features9",
                    },
                    Name:                  "name6",
                    Sizes:                 []string{
                        "sizes6",
                    },
                    Slug:                  "slug0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Size:                  models.Size{
                    Available:             false,
                    Description:           "description0",
                    Disk:                  252,
                    Memory:                168,
                    PriceHourly:           float64(121.04),
                    PriceMonthly:          float64(162.04),
                    Regions:               []string{
                        "regions5",
                    },
                    Slug:                  "slug6",
                    Transfer:              float64(150.78),
                    Vcpus:                 234,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                SizeSlug:              "size_slug0",
                SnapshotIds:           []int{
                    93,
                    94,
                },
                Status:                models.Status8_New,
                Tags:                  []string{
                    "tags5",
                },
                Vcpus:                 80,
                VolumeIds:             []string{
                    "volume_ids0",
                    "volume_ids1",
                    "volume_ids2",
                },
                VpcUuid:               models.ToPointer("vpc_uuid0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Droplet{
                BackupIds:             []int{
                    104,
                    105,
                },
                CreatedAt:             parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) }),
                Disk:                  98,
                Features:              []string{
                    "features1",
                    "features2",
                    "features3",
                },
                Id:                    232,
                Image:                 models.Image1{
                    CreatedAt:             models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    Description:           models.ToPointer("description6"),
                    Distribution:          models.ToPointer(models.Distribution_Coreos),
                    ErrorMessage:          models.ToPointer("error_message8"),
                    Id:                    models.ToPointer(128),
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
                Memory:                16,
                Name:                  "name0",
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
                    End:                   models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    Start:                 models.ToPointer(parseTime(time.RFC3339, "2016-03-13T12:52:32.123Z", func(err error) { log.Fatalln(err) })),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Region:                models.Region{
                    Available:             false,
                    Features:              []string{
                        "features7",
                        "features8",
                        "features9",
                    },
                    Name:                  "name6",
                    Sizes:                 []string{
                        "sizes6",
                    },
                    Slug:                  "slug0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Size:                  models.Size{
                    Available:             false,
                    Description:           "description0",
                    Disk:                  252,
                    Memory:                168,
                    PriceHourly:           float64(121.04),
                    PriceMonthly:          float64(162.04),
                    Regions:               []string{
                        "regions5",
                    },
                    Slug:                  "slug6",
                    Transfer:              float64(150.78),
                    Vcpus:                 234,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                SizeSlug:              "size_slug0",
                SnapshotIds:           []int{
                    93,
                    94,
                },
                Status:                models.Status8_New,
                Tags:                  []string{
                    "tags5",
                },
                Vcpus:                 80,
                VolumeIds:             []string{
                    "volume_ids0",
                    "volume_ids1",
                    "volume_ids2",
                },
                VpcUuid:               models.ToPointer("vpc_uuid0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



