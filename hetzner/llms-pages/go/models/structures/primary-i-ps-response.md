# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ


# Class Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/meta.md) | Optional | - |
| `PrimaryIps` | [`[]models.PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/primary-ip-1.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    primaryIPsResponse := models.PrimaryIPsResponse{
        Meta:                 models.ToPointer(models.Meta{
            Pagination:           models.Pagination{
                LastPage:             models.ToPointer(float64(77.7)),
                NextPage:             models.ToPointer(float64(209.18)),
                Page:                 float64(17.58),
                PerPage:              float64(13.34),
                PreviousPage:         models.ToPointer(float64(50.02)),
                TotalEntries:         models.ToPointer(float64(206.64)),
            },
        }),
        PrimaryIps:           []models.PrimaryIP1{
            models.PrimaryIP1{
                AssigneeId:           models.ToPointer(17),
                AssigneeType:         "server",
                AutoDelete:           true,
                Blocked:              false,
                Created:              "2016-01-30T23:55:00+00:00",
                Datacenter:           models.Datacenter2{
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
                DnsPtr:               []models.DnsPtr{
                    models.DnsPtr{
                        DnsPtr:               "server.example.com",
                        Ip:                   "2001:db8::1",
                    },
                },
                Id:                   42,
                Ip:                   "131.232.99.1",
                Labels:               map[string]string{
                    "key0": "labels2",
                    "key1": "labels3",
                    "key2": "labels4",
                },
                Name:                 "my-resource",
                Protection:           models.Protection{
                    Delete:               false,
                },
                Type:                 models.Type50Enum_IPV4,
            },
        },
    }

}
```



