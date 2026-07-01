# Servers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`ServersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `Servers` | [`[]models.Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-18.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serversResponse := models.ServersResponse{
        Meta:                  models.ToPointer(models.Meta{
            Pagination:            models.Pagination{
                LastPage:              models.ToPointer(float64(77.7)),
                NextPage:              models.ToPointer(float64(209.18)),
                Page:                  float64(17.58),
                PerPage:               float64(13.34),
                PreviousPage:          models.ToPointer(float64(50.02)),
                TotalEntries:          models.ToPointer(float64(206.64)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        Servers:               []models.Server18{
            models.Server18{
                BackupWindow:          models.ToPointer("22-02"),
                Created:               "2016-01-30T23:55:00+00:00",
                Datacenter:            models.Datacenter6{
                    Description:           "Falkenstein DC Park 8",
                    Id:                    42,
                    Location:              models.Location{
                        City:                  "Falkenstein",
                        Country:               "DE",
                        Description:           "Falkenstein DC Park 1",
                        Id:                    float64(1),
                        Latitude:              float64(50.47612),
                        Longitude:             float64(12.370071),
                        Name:                  "fsn1",
                        NetworkZone:           "eu-central",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    Name:                  "fsn1-dc8",
                    ServerTypes:           models.ServerTypes{
                        Available:             []float64{
                            float64(1),
                            float64(2),
                            float64(3),
                        },
                        AvailableForMigration: []float64{
                            float64(1),
                            float64(2),
                            float64(3),
                        },
                        Supported:             []float64{
                            float64(1),
                            float64(2),
                            float64(3),
                        },
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Id:                    42,
                Image:                 models.ToPointer(models.Image{
                    BoundTo:               nil,
                    Created:               "2016-01-30T23:55:00+00:00",
                    CreatedFrom:           models.ToPointer(models.CreatedFrom{
                        Id:                    1,
                        Name:                  "Server",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Deleted:               nil,
                    Deprecated:            models.ToPointer("2018-02-28T00:00:00+00:00"),
                    Description:           "Ubuntu 20.04 Standard 64 bit",
                    DiskSize:              float64(10),
                    Id:                    42,
                    ImageSize:             models.ToPointer(float64(2.3)),
                    Labels:                map[string]string{
                        "key0": "labels4",
                    },
                    Name:                  models.ToPointer("ubuntu-20.04"),
                    OsFlavor:              models.OsFlavor_Ubuntu,
                    OsVersion:             models.ToPointer("20.04"),
                    Protection:            models.Protection{
                        Delete:                false,
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    RapidDeploy:           models.ToPointer(false),
                    Status:                models.Status24_Unavailable,
                    Type:                  models.Type22_Snapshot,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                IncludedTraffic:       models.ToPointer(float64(654321)),
                IngoingTraffic:        models.ToPointer(float64(123456)),
                Iso:                   models.ToPointer(models.Iso2{
                    Deprecated:            models.ToPointer("2018-02-28T00:00:00+00:00"),
                    Description:           "FreeBSD 11.0 x64",
                    Id:                    42,
                    Name:                  models.ToPointer("FreeBSD-11.0-RELEASE-amd64-dvd1"),
                    Type:                  models.Type26_Public,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Labels:                map[string]string{
                    "key0": "labels0",
                },
                LoadBalancers:         []int{
                    128,
                    129,
                    130,
                },
                Locked:                false,
                Name:                  "my-resource",
                OutgoingTraffic:       models.ToPointer(float64(123456)),
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
                PrimaryDiskSize:       float64(50),
                PrivateNet:            []models.PrivateNet4{
                    models.PrivateNet4{
                        AliasIps:              []string{
                            "alias_ips4",
                        },
                        Ip:                    models.ToPointer("10.0.0.2"),
                        MacAddress:            models.ToPointer("86:00:ff:2a:7d:e1"),
                        Network:               models.ToPointer(4711),
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
                        478,
                    },
                    Ipv4:                  models.ToPointer(models.Ipv44{
                        Blocked:               false,
                        DnsPtr:                "server01.example.com",
                        Id:                    models.ToPointer(42),
                        Ip:                    "1.2.3.4",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    }),
                    Ipv6:                  models.ToPointer(models.Ipv64{
                        Blocked:               false,
                        DnsPtr:                []models.DnsPtr8{
                            models.DnsPtr8{
                                DnsPtr:                "server.example.com",
                                Ip:                    "2001:db8::1",
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                        },
                        Id:                    models.ToPointer(42),
                        Ip:                    "2001:db8::/64",
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
                    Cores:                 float64(1),
                    CpuType:               models.CpuType_Shared,
                    Deprecated:            false,
                    Description:           "CX11",
                    Disk:                  float64(25),
                    Id:                    1,
                    Memory:                float64(1),
                    Name:                  "cx11",
                    Prices:                []models.Price9{
                        models.Price9{
                            Location:              "fsn1",
                            PriceHourly:           models.PriceHourly8{
                                Gross:                 "1.1900000000000000",
                                Net:                   "1.0000000000",
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                            PriceMonthly:          models.PriceMonthly10{
                                Gross:                 "1.1900000000000000",
                                Net:                   "1.0000000000",
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
                    177,
                },
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



