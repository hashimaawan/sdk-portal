# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Server` | [`*models.Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-18.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversResponse2 := models.ServersResponse2{
        Server:                models.ToPointer(models.Server18{
            BackupWindow:          models.ToPointer("backup_window2"),
            Created:               "created4",
            Datacenter:            models.Datacenter6{
                Description:           "description0",
                Id:                    200,
                Location:              models.Location{
                    City:                  "city6",
                    Country:               "country8",
                    Description:           "description6",
                    Id:                    float64(187.14),
                    Latitude:              float64(194.62),
                    Longitude:             float64(59.18),
                    Name:                  "name4",
                    NetworkZone:           "network_zone2",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Name:                  "name0",
                ServerTypes:           models.ServerTypes{
                    Available:             []float64{
                        float64(23.74),
                    },
                    AvailableForMigration: []float64{
                        float64(201.65),
                        float64(201.66),
                    },
                    Supported:             []float64{
                        float64(69.52),
                        float64(69.53),
                        float64(69.54),
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            Id:                    14,
            Image:                 models.ToPointer(models.Image{
                BoundTo:               models.ToPointer(186),
                Created:               "created6",
                CreatedFrom:           models.ToPointer(models.CreatedFrom{
                    Id:                    60,
                    Name:                  "name6",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Deleted:               models.ToPointer("deleted4"),
                Deprecated:            models.ToPointer("deprecated8"),
                Description:           "description6",
                DiskSize:              float64(244.18),
                Id:                    128,
                ImageSize:             models.ToPointer(float64(141.34)),
                Labels:                map[string]string{
                    "key0": "labels4",
                },
                Name:                  models.ToPointer("name6"),
                OsFlavor:              models.OsFlavor_Debian,
                OsVersion:             models.ToPointer("os_version4"),
                Protection:            models.Protection{
                    Delete:                false,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                RapidDeploy:           models.ToPointer(false),
                Status:                models.Status24_Unavailable,
                Type:                  models.Type22_App,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            IncludedTraffic:       models.ToPointer(float64(123.68)),
            IngoingTraffic:        models.ToPointer(float64(151.82)),
            Iso:                   models.ToPointer(models.Iso2{
                Deprecated:            models.ToPointer("deprecated0"),
                Description:           "description2",
                Id:                    66,
                Name:                  models.ToPointer("name8"),
                Type:                  models.Type26_Public,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            }),
            Labels:                map[string]string{
                "key0": "labels0",
                "key1": "labels9",
            },
            LoadBalancers:         []int{
                144,
                143,
                142,
            },
            Locked:                false,
            Name:                  "name4",
            OutgoingTraffic:       models.ToPointer(float64(129.6)),
            PlacementGroup:        models.NewOptional(models.ToPointer(models.PlacementGroupNullable{
                Created:               "created8",
                Id:                    236,
                Labels:                map[string]string{
                    "key0": "labels4",
                },
                Name:                  "name8",
                Servers:               []int{
                    251,
                    252,
                    253,
                },
                Type:                  "type2",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            })),
            PrimaryDiskSize:       float64(19.88),
            PrivateNet:            []models.PrivateNet4{
                models.PrivateNet4{
                    AliasIps:              []string{
                        "alias_ips4",
                    },
                    Ip:                    models.ToPointer("ip6"),
                    MacAddress:            models.ToPointer("mac_address0"),
                    Network:               models.ToPointer(154),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                models.PrivateNet4{
                    AliasIps:              []string{
                        "alias_ips4",
                    },
                    Ip:                    models.ToPointer("ip6"),
                    MacAddress:            models.ToPointer("mac_address0"),
                    Network:               models.ToPointer(154),
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
            },
            Protection:            models.Protection20{
                Delete:                false,
                Rebuild:               false,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            PublicNet:             models.PublicNet4{
                Firewalls:             []models.ServerPublicNetFirewall{
                    models.ServerPublicNetFirewall{
                        Id:                    models.ToPointer(250),
                        Status:                models.ToPointer(models.Status72_Applied),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    models.ServerPublicNetFirewall{
                        Id:                    models.ToPointer(250),
                        Status:                models.ToPointer(models.Status72_Applied),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                FloatingIps:           []int{
                    54,
                    55,
                    56,
                },
                Ipv4:                  models.ToPointer(models.Ipv44{
                    Blocked:               false,
                    DnsPtr:                "dns_ptr4",
                    Id:                    models.ToPointer(104),
                    Ip:                    "ip2",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Ipv6:                  models.ToPointer(models.Ipv64{
                    Blocked:               false,
                    DnsPtr:                []models.DnsPtr8{
                        models.DnsPtr8{
                            DnsPtr:                "dns_ptr0",
                            Ip:                    "ip6",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        models.DnsPtr8{
                            DnsPtr:                "dns_ptr0",
                            Ip:                    "ip6",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                    },
                    Id:                    models.ToPointer(8),
                    Ip:                    "ip0",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            RescueEnabled:         false,
            ServerType:            models.ServerType1{
                Cores:                 float64(12.84),
                CpuType:               models.CpuType_Shared,
                Deprecated:            false,
                Description:           "description0",
                Disk:                  float64(14.32),
                Id:                    30,
                Memory:                float64(21.2),
                Name:                  "name0",
                Prices:                []models.Price9{
                    models.Price9{
                        Location:              "location8",
                        PriceHourly:           models.PriceHourly8{
                            Gross:                 "gross4",
                            Net:                   "net2",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        PriceMonthly:          models.PriceMonthly10{
                            Gross:                 "gross2",
                            Net:                   "net0",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                StorageType:           models.StorageType_Local,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            Status:                models.Status73_Starting,
            Volumes:               []int{
                91,
                92,
            },
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



