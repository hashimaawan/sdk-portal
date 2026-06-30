# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Pricing` | [`models.Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/pricing.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    pricingResponse := models.PricingResponse{
        Pricing:              models.Pricing{
            Currency:          "EUR",
            FloatingIp:        models.FloatingIp4{
                PriceMonthly:         models.PriceMonthly6{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
            },
            FloatingIps:       []models.FloatingIp5{
                models.FloatingIp5{
                    Prices:               []models.Price6{
                        models.Price6{
                            Location:             "fsn1",
                            PriceMonthly:         models.PriceMonthly7{
                                Gross:                "1.1900000000000000",
                                Net:                  "1.0000000000",
                            },
                        },
                    },
                    Type:                 models.Type48Enum_IPV4,
                },
            },
            Image:             models.Image3{
                PricePerGbMonth:      models.PricePerGbMonth{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
            },
            LoadBalancerTypes: []models.LoadBalancerType6{
                models.LoadBalancerType6{
                    Id:                   float64(1),
                    Name:                 "lb11",
                    Prices:               []models.Price7{
                        models.Price7{
                            Location:             "fsn1",
                            PriceHourly:          models.PriceHourly6{
                                Gross:                "1.1900000000000000",
                                Net:                  "1.0000000000",
                            },
                            PriceMonthly:         models.PriceMonthly8{
                                Gross:                "1.1900000000000000",
                                Net:                  "1.0000000000",
                            },
                        },
                    },
                },
            },
            PrimaryIps:        []models.PrimaryIp{
                models.PrimaryIp{
                    Prices:               []models.Price8{
                        models.Price8{
                            Location:             "fsn1",
                            PriceHourly:          models.PriceHourly7{
                                Gross:                "1.1900000000000000",
                                Net:                  "1.0000000000",
                            },
                            PriceMonthly:         models.PriceMonthly9{
                                Gross:                "1.1900000000000000",
                                Net:                  "1.0000000000",
                            },
                        },
                    },
                    Type:                 models.Type49Enum_IPV4,
                },
            },
            ServerBackup:      models.ServerBackup{
                Percentage:           "20.0000000000",
            },
            ServerTypes:       []models.ServerTypes2{
                models.ServerTypes2{
                    Id:                   float64(4),
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
                },
            },
            Traffic:           models.Traffic{
                PricePerTb:           models.PricePerTb{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
            },
            VatRate:           "19.000000",
            Volume:            models.Volume{
                PricePerGbMonth:      models.PricePerGbMonth{
                    Gross:                "1.1900000000000000",
                    Net:                  "1.0000000000",
                },
            },
        },
    }

}
```



