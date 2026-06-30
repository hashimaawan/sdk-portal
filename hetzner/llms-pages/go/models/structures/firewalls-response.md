# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewalls` | [`[]models.Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/firewall.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/meta.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    firewallsResponse := models.FirewallsResponse{
        Firewalls:            []models.Firewall{
            models.Firewall{
                AppliedTo:            []models.AppliedTo{
                    models.AppliedTo{
                        AppliedToResources:   []models.AppliedToResource{
                            models.AppliedToResource{
                                Server:               models.ToPointer(models.Server{
                                    Id:                   14,
                                }),
                                Type:                 models.ToPointer(models.Type5Enum_SERVER),
                            },
                        },
                        LabelSelector:        models.ToPointer(models.LabelSelector{
                            Selector:             "selector8",
                        }),
                        Server:               models.ToPointer(models.Server{
                            Id:                   14,
                        }),
                        Type:                 models.Type6Enum_SERVER,
                    },
                },
                Created:              "2016-01-30T23:55:00+00:00",
                Id:                   42,
                Labels:               map[string]string{
                    "key0": "labels4",
                    "key1": "labels5",
                },
                Name:                 "my-resource",
                Rules:                []models.Rule{
                    models.Rule{
                        Description:          models.NewOptional(models.ToPointer("description2")),
                        DestinationIps:       []string{
                            "28.239.13.1/32",
                            "28.239.14.0/24",
                            "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                        },
                        Direction:            models.DirectionEnum_IN,
                        Port:                 models.ToPointer("80"),
                        Protocol:             models.ProtocolEnum_UDP,
                        SourceIps:            []string{
                            "28.239.13.1/32",
                            "28.239.14.0/24",
                            "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                        },
                    },
                },
            },
        },
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
    }

}
```



