# Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `LoadBalancers` | [`[]models.LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/load-balancer.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    loadBalancersResponse := models.LoadBalancersResponse{
        LoadBalancers:         []models.LoadBalancer{
            models.LoadBalancer{
                Algorithm:             models.Algorithm{
                    Type:                  models.Type28_RoundRobin,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Created:               "2016-01-30T23:55:00+00:00",
                Id:                    42,
                IncludedTraffic:       10000,
                IngoingTraffic:        models.ToPointer(204),
                Labels:                map[string]string{
                    "key0": "labels8",
                    "key1": "labels7",
                    "key2": "labels6",
                },
                LoadBalancerType:      models.LoadBalancerType{
                    Deprecated:              models.ToPointer("2016-01-30T23:50:00+00:00"),
                    Description:             "LB11",
                    Id:                      float64(1),
                    MaxAssignedCertificates: float64(10),
                    MaxConnections:          float64(20000),
                    MaxServices:             float64(5),
                    MaxTargets:              float64(25),
                    Name:                    "lb11",
                    Prices:                  []models.Price{
                        models.Price{
                            Location:              "fsn1",
                            PriceHourly:           models.PriceHourly{
                                Gross:                 "1.1900000000000000",
                                Net:                   "1.0000000000",
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                            PriceMonthly:          models.PriceMonthly{
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
                    AdditionalProperties:    map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
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
                Name:                  "my-resource",
                OutgoingTraffic:       models.ToPointer(30),
                PrivateNet:            []models.PrivateNet{
                    models.PrivateNet{
                        Ip:                    models.ToPointer("10.0.0.2"),
                        Network:               models.ToPointer(4711),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Protection:            models.Protection{
                    Delete:                false,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                PublicNet:             models.PublicNet{
                    Enabled:               false,
                    Ipv4:                  models.Ipv4{
                        DnsPtr:                models.NewOptional(models.ToPointer("lb1.example.com")),
                        Ip:                    models.NewOptional(models.ToPointer("1.2.3.4")),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    Ipv6:                  models.Ipv6{
                        DnsPtr:                models.NewOptional(models.ToPointer("lb1.example.com")),
                        Ip:                    models.NewOptional(models.ToPointer("2001:db8::1")),
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Services:              []models.LoadBalancerService{
                    models.LoadBalancerService{
                        DestinationPort:       80,
                        HealthCheck:           models.LoadBalancerServiceHealthCheck{
                            Http:     models.ToPointer(models.Http{
                                Domain:      models.ToPointer("domain4"),
                                Path:        "path2",
                                Response:    models.ToPointer("response8"),
                                StatusCodes: []string{
                                    "status_codes0",
                                    "status_codes1",
                                    "status_codes2",
                                },
                                Tls:         models.ToPointer(false),
                            }),
                            Interval: 15,
                            Port:     4711,
                            Protocol: models.Protocol6_Http,
                            Retries:  3,
                            Timeout:  10,
                        },
                        Http:                  models.ToPointer(models.LoadBalancerServiceHttp{
                            Certificates:          []int{
                                180,
                            },
                            CookieLifetime:        models.ToPointer(160),
                            CookieName:            models.ToPointer("cookie_name6"),
                            RedirectHttp:          models.ToPointer(false),
                            StickySessions:        models.ToPointer(false),
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        ListenPort:            443,
                        Protocol:              models.Protocol7_Https,
                        Proxyprotocol:         false,
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Targets:               []models.LoadBalancerTarget{
                    models.LoadBalancerTarget{
                        HealthStatus:          []models.HealthStatus{
                            models.HealthStatus{
                                ListenPort:            models.ToPointer(142),
                                Status:                models.ToPointer(models.Status30_Unknown),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                            models.HealthStatus{
                                ListenPort:            models.ToPointer(142),
                                Status:                models.ToPointer(models.Status30_Unknown),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                        },
                        Ip:                    models.ToPointer(models.Ip{
                            Ip:                    "ip8",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        LabelSelector:         models.ToPointer(models.LabelSelector7{
                            Selector:              "selector8",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Server:                models.ToPointer(models.LoadBalancerTargetServer{
                            Id:                    14,
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        }),
                        Targets:               []models.Target{
                            models.Target{
                                HealthStatus:          []models.HealthStatus{
                                    models.HealthStatus{
                                        ListenPort:            models.ToPointer(142),
                                        Status:                models.ToPointer(models.Status30_Unknown),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    },
                                    models.HealthStatus{
                                        ListenPort:            models.ToPointer(142),
                                        Status:                models.ToPointer(models.Status30_Unknown),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    },
                                },
                                Server:                models.ToPointer(models.Server11{
                                    Id:                    14,
                                    AdditionalProperties:  map[string]interface{}{
                                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                    },
                                }),
                                Type:                  models.ToPointer("type2"),
                                UsePrivateIp:          models.ToPointer(false),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                            models.Target{
                                HealthStatus:          []models.HealthStatus{
                                    models.HealthStatus{
                                        ListenPort:            models.ToPointer(142),
                                        Status:                models.ToPointer(models.Status30_Unknown),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    },
                                    models.HealthStatus{
                                        ListenPort:            models.ToPointer(142),
                                        Status:                models.ToPointer(models.Status30_Unknown),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    },
                                },
                                Server:                models.ToPointer(models.Server11{
                                    Id:                    14,
                                    AdditionalProperties:  map[string]interface{}{
                                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                    },
                                }),
                                Type:                  models.ToPointer("type2"),
                                UsePrivateIp:          models.ToPointer(false),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                            models.Target{
                                HealthStatus:          []models.HealthStatus{
                                    models.HealthStatus{
                                        ListenPort:            models.ToPointer(142),
                                        Status:                models.ToPointer(models.Status30_Unknown),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    },
                                    models.HealthStatus{
                                        ListenPort:            models.ToPointer(142),
                                        Status:                models.ToPointer(models.Status30_Unknown),
                                        AdditionalProperties:  map[string]interface{}{
                                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                        },
                                    },
                                },
                                Server:                models.ToPointer(models.Server11{
                                    Id:                    14,
                                    AdditionalProperties:  map[string]interface{}{
                                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                    },
                                }),
                                Type:                  models.ToPointer("type2"),
                                UsePrivateIp:          models.ToPointer(false),
                                AdditionalProperties:  map[string]interface{}{
                                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                                },
                            },
                        },
                        Type:                  models.Type29_Ip,
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



