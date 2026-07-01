# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Currency` | `string` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 |
| `FloatingIp` | [`models.FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month |
| `FloatingIps` | [`[]models.FloatingIp5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type |
| `Image` | [`models.Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/image-3.md) | Required | The cost of Image per GB/month |
| `LoadBalancerTypes` | [`[]models.LoadBalancerType6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type |
| `PrimaryIps` | [`[]models.PrimaryIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location |
| `ServerBackup` | [`models.ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage |
| `ServerTypes` | [`[]models.ServerTypes2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type |
| `Traffic` | [`models.Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/traffic.md) | Required | The cost of additional traffic per TB |
| `VatRate` | `string` | Required | The VAT rate used for calculating prices with VAT |
| `Volume` | [`models.Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/volume.md) | Required | The cost of Volume per GB/month |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    pricing := models.Pricing{
        Currency:          "EUR",
        FloatingIp:        models.FloatingIp4{
            PriceMonthly:          models.PriceMonthly6{
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
        FloatingIps:       []models.FloatingIp5{
            models.FloatingIp5{
                Prices:                []models.Price6{
                    models.Price6{
                        Location:              "fsn1",
                        PriceMonthly:          models.PriceMonthly7{
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
                Type:                  models.Type48_Ipv4,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Image:             models.Image3{
            PricePerGbMonth:       models.PricePerGbMonth{
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
        LoadBalancerTypes: []models.LoadBalancerType6{
            models.LoadBalancerType6{
                Id:                    float64(1),
                Name:                  "lb11",
                Prices:                []models.Price7{
                    models.Price7{
                        Location:              "fsn1",
                        PriceHourly:           models.PriceHourly6{
                            Gross:                 "1.1900000000000000",
                            Net:                   "1.0000000000",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        PriceMonthly:          models.PriceMonthly8{
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
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        PrimaryIps:        []models.PrimaryIp{
            models.PrimaryIp{
                Prices:                []models.Price8{
                    models.Price8{
                        Location:              "fsn1",
                        PriceHourly:           models.PriceHourly7{
                            Gross:                 "1.1900000000000000",
                            Net:                   "1.0000000000",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        PriceMonthly:          models.PriceMonthly9{
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
                Type:                  models.Type49_Ipv4,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        ServerBackup:      models.ServerBackup{
            Percentage:            "20.0000000000",
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        ServerTypes:       []models.ServerTypes2{
            models.ServerTypes2{
                Id:                    float64(4),
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
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Traffic:           models.Traffic{
            PricePerTb:            models.PricePerTb{
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
        VatRate:           "19.000000",
        Volume:            models.Volume{
            PricePerGbMonth:       models.PricePerGbMonth{
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
    }

}
```



