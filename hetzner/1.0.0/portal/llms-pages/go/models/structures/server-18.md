# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlcjE4


# Class Name

`Server18`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `BackupWindow` | `*string` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Datacenter` | [`models.Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at |
| `Id` | `int` | Required | ID of the Resource |
| `Image` | [`*models.Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/image.md) | Required | - |
| `IncludedTraffic` | `*float64` | Required | Free Traffic for the current billing period in bytes |
| `IngoingTraffic` | `*float64` | Required | Inbound Traffic for the current billing period in bytes |
| `Iso` | [`*models.Iso2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `LoadBalancers` | `[]int` | Optional | - |
| `Locked` | `bool` | Required | True if Server has been locked and is not available to user |
| `Name` | `string` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) |
| `OutgoingTraffic` | `*float64` | Required | Outbound Traffic for the current billing period in bytes |
| `PlacementGroup` | [`models.Optional[models.PlacementGroupNullable]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/placement-group-nullable.md) | Optional | - |
| `PrimaryDiskSize` | `float64` | Required | Size of the primary Disk |
| `PrivateNet` | [`[]models.PrivateNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/private-net-4.md) | Required | Private networks information |
| `Protection` | [`models.Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/protection-20.md) | Required | Protection configuration for the Server |
| `PublicNet` | [`models.PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` |
| `RescueEnabled` | `bool` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot |
| `ServerType` | [`models.ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has |
| `Status` | [`models.Status73Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/status-73.md) | Required | Status of the Server |
| `Volumes` | `[]int` | Optional | IDs of Volumes assigned to this Server |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    server18 := models.Server18{
        BackupWindow:         models.ToPointer("22-02"),
        Created:              "2016-01-30T23:55:00+00:00",
        Datacenter:           models.Datacenter6{
            Description:          "Falkenstein DC Park 8",
            Id:                   42,
            Location:             models.Location{
                City:                 "Falkenstein",
                Country:              "DE",
                Description:          "Falkenstein DC Park 1",
                Id:                   float64(1),
                Latitude:             float64(50.47612),
                Longitude:            float64(12.370071),
                Name:                 "fsn1",
                NetworkZone:          "eu-central",
            },
            Name:                 "fsn1-dc8",
            ServerTypes:          models.ServerTypes{
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
            },
        },
        Id:                   42,
        Image:                models.ToPointer(models.Image{
            BoundTo:              nil,
            Created:              "2016-01-30T23:55:00+00:00",
            CreatedFrom:          models.ToPointer(models.CreatedFrom{
                Id:                   1,
                Name:                 "Server",
            }),
            Deleted:              nil,
            Deprecated:           models.ToPointer("2018-02-28T00:00:00+00:00"),
            Description:          "Ubuntu 20.04 Standard 64 bit",
            DiskSize:             float64(10),
            Id:                   42,
            ImageSize:            models.ToPointer(float64(2.3)),
            Labels:               map[string]string{
                "key0": "labels4",
            },
            Name:                 models.ToPointer("ubuntu-20.04"),
            OsFlavor:             models.OsFlavorEnum_UBUNTU,
            OsVersion:            models.ToPointer("20.04"),
            Protection:           models.Protection{
                Delete:               false,
            },
            RapidDeploy:          models.ToPointer(false),
            Status:               models.Status24Enum_UNAVAILABLE,
            Type:                 models.Type22Enum_SNAPSHOT,
        }),
        IncludedTraffic:      models.ToPointer(float64(654321)),
        IngoingTraffic:       models.ToPointer(float64(123456)),
        Iso:                  models.ToPointer(models.Iso2{
            Deprecated:           models.ToPointer("2018-02-28T00:00:00+00:00"),
            Description:          "FreeBSD 11.0 x64",
            Id:                   42,
            Name:                 models.ToPointer("FreeBSD-11.0-RELEASE-amd64-dvd1"),
            Type:                 models.Type26Enum_PUBLIC,
        }),
        Labels:               map[string]string{
            "key0": "labels4",
            "key1": "labels3",
            "key2": "labels2",
        },
        LoadBalancers:        []int{
            248,
        },
        Locked:               false,
        Name:                 "my-resource",
        OutgoingTraffic:      models.ToPointer(float64(123456)),
        PlacementGroup:       models.NewOptional(models.ToPointer(models.PlacementGroupNullable{
            Created:              "created8",
            Id:                   236,
            Labels:               map[string]string{
                "key0": "labels4",
            },
            Name:                 "name8",
            Servers:              []int{
                251,
                252,
                253,
            },
            Type:                 "type2",
        })),
        PrimaryDiskSize:      float64(50),
        PrivateNet:           []models.PrivateNet4{
            models.PrivateNet4{
                AliasIps:             []string{
                    "alias_ips4",
                },
                Ip:                   models.ToPointer("10.0.0.2"),
                MacAddress:           models.ToPointer("86:00:ff:2a:7d:e1"),
                Network:              models.ToPointer(4711),
            },
        },
        Protection:           models.Protection20{
            Delete:               false,
            Rebuild:              false,
        },
        PublicNet:            models.PublicNet4{
            Firewalls:            []models.ServerPublicNetFirewall{
                models.ServerPublicNetFirewall{
                    Id:                   models.ToPointer(250),
                    Status:               models.ToPointer(models.Status72Enum_APPLIED),
                },
                models.ServerPublicNetFirewall{
                    Id:                   models.ToPointer(250),
                    Status:               models.ToPointer(models.Status72Enum_APPLIED),
                },
            },
            FloatingIps:          []int{
                478,
            },
            Ipv4:                 models.ToPointer(models.Ipv44{
                Blocked:              false,
                DnsPtr:               "server01.example.com",
                Id:                   models.ToPointer(42),
                Ip:                   "1.2.3.4",
            }),
            Ipv6:                 models.ToPointer(models.Ipv64{
                Blocked:              false,
                DnsPtr:               []models.DnsPtr8{
                    models.DnsPtr8{
                        DnsPtr:               "server.example.com",
                        Ip:                   "2001:db8::1",
                    },
                },
                Id:                   models.ToPointer(42),
                Ip:                   "2001:db8::/64",
            }),
        },
        RescueEnabled:        false,
        ServerType:           models.ServerType1{
            Cores:                float64(1),
            CpuType:              models.CpuTypeEnum_SHARED,
            Deprecated:           false,
            Description:          "CX11",
            Disk:                 float64(25),
            Id:                   1,
            Memory:               float64(1),
            Name:                 "cx11",
            Prices:               []models.Price9{
                models.Price9{
                    Location:             "fsn1",
                    PriceHourly:          models.PriceHourly8{
                        Gross:                "1.1900000000000000",
                        Net:                  "1.0000000000",
                    },
                    PriceMonthly:         models.PriceMonthly10{
                        Gross:                "1.1900000000000000",
                        Net:                  "1.0000000000",
                    },
                },
            },
            StorageType:          models.StorageTypeEnum_LOCAL,
        },
        Status:               models.Status73Enum_RUNNING,
        Volumes:              []int{
            199,
            200,
            201,
        },
    }

}
```



