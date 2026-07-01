# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewalls` | [`[]models.Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    firewallsResponse := models.FirewallsResponse{
        Firewalls:             []models.Firewall{
            models.Firewall{
                AppliedTo:             []models.AppliedTo{
                    models.AppliedTo{
                        AppliedToResources:    []models.AppliedToResource{
                            models.AppliedToResource{
                                Server:                models.ToPointer(models.Server{
                                    Id:                    14,
                                    AdditionalProperties:  map[string]interface{}{
                                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                    },
                                }),
                                Type:                  models.ToPointer(models.Type5_Server),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                        },
                        LabelSelector:         models.ToPointer(models.LabelSelector{
                            Selector:              "selector8",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Server:                models.ToPointer(models.Server{
                            Id:                    14,
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Type:                  models.Type6_Server,
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Created:               "2016-01-30T23:55:00+00:00",
                Id:                    42,
                Labels:                map[string]string{
                    "key0": "labels4",
                    "key1": "labels5",
                },
                Name:                  "my-resource",
                Rules:                 []models.Rule{
                    models.Rule{
                        Description:           models.NewOptional(models.ToPointer("description2")),
                        DestinationIps:        []string{
                            "28.239.13.1/32",
                            "28.239.14.0/24",
                            "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                        },
                        Direction:             models.Direction_In,
                        Port:                  models.ToPointer("80"),
                        Protocol:              models.Protocol_Udp,
                        SourceIps:             []string{
                            "28.239.13.1/32",
                            "28.239.14.0/24",
                            "ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128",
                        },
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
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
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



