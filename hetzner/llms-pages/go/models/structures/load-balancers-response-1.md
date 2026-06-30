# Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/action.md) | Required | - |
| `LoadBalancer` | [`models.LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/load-balancer.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    loadBalancersResponse1 := models.LoadBalancersResponse1{
        Action:               models.Action{
            Command:              "start_server",
            Error:                models.ToPointer(models.Error{
                Code:                 "action_failed",
                Message:              "Action failed",
            }),
            Finished:             models.ToPointer("2016-01-30T23:55:00+00:00"),
            Id:                   42,
            Progress:             float64(100),
            Resources:            []models.Resource{
                models.Resource{
                    Id:                   42,
                    Type:                 "server",
                },
            },
            Started:              "2016-01-30T23:55:00+00:00",
            Status:               models.StatusEnum_RUNNING,
        },
        LoadBalancer:         models.LoadBalancer{
            Algorithm:            models.Algorithm{
                Type:                 models.Type28Enum_ROUNDROBIN,
            },
            Created:              "2016-01-30T23:55:00+00:00",
            Id:                   42,
            IncludedTraffic:      10000,
            IngoingTraffic:       models.ToPointer(216),
            Labels:               map[string]string{
                "key0": "labels2",
                "key1": "labels1",
            },
            LoadBalancerType:     models.LoadBalancerType{
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
                        Location:             "fsn1",
                        PriceHourly:          models.PriceHourly{
                            Gross:                "1.1900000000000000",
                            Net:                  "1.0000000000",
                        },
                        PriceMonthly:         models.PriceMonthly{
                            Gross:                "1.1900000000000000",
                            Net:                  "1.0000000000",
                        },
                    },
                },
            },
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
            Name:                 "my-resource",
            OutgoingTraffic:      models.ToPointer(42),
            PrivateNet:           []models.PrivateNet{
                models.PrivateNet{
                    Ip:                   models.ToPointer("10.0.0.2"),
                    Network:              models.ToPointer(4711),
                },
            },
            Protection:           models.Protection{
                Delete:               false,
            },
            PublicNet:            models.PublicNet{
                Enabled:              false,
                Ipv4:                 models.Ipv4{
                    DnsPtr:               models.NewOptional(models.ToPointer("lb1.example.com")),
                    Ip:                   models.NewOptional(models.ToPointer("1.2.3.4")),
                },
                Ipv6:                 models.Ipv6{
                    DnsPtr:               models.NewOptional(models.ToPointer("lb1.example.com")),
                    Ip:                   models.NewOptional(models.ToPointer("2001:db8::1")),
                },
            },
            Services:             []models.LoadBalancerService{
                models.LoadBalancerService{
                    DestinationPort:      80,
                    HealthCheck:          models.LoadBalancerServiceHealthCheck{
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
                        Protocol: models.Protocol6Enum_HTTP,
                        Retries:  3,
                        Timeout:  10,
                    },
                    Http:                 models.ToPointer(models.LoadBalancerServiceHTTP{
                        Certificates:         []int{
                            180,
                        },
                        CookieLifetime:       models.ToPointer(160),
                        CookieName:           models.ToPointer("cookie_name6"),
                        RedirectHttp:         models.ToPointer(false),
                        StickySessions:       models.ToPointer(false),
                    }),
                    ListenPort:           443,
                    Protocol:             models.Protocol7Enum_HTTPS,
                    Proxyprotocol:        false,
                },
            },
            Targets:              []models.LoadBalancerTarget{
                models.LoadBalancerTarget{
                    HealthStatus:         []models.HealthStatus{
                        models.HealthStatus{
                            ListenPort:           models.ToPointer(142),
                            Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                        },
                        models.HealthStatus{
                            ListenPort:           models.ToPointer(142),
                            Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                        },
                    },
                    Ip:                   models.ToPointer(models.Ip{
                        Ip:                   "ip8",
                    }),
                    LabelSelector:        models.ToPointer(models.LabelSelector7{
                        Selector:             "selector8",
                    }),
                    Server:               models.ToPointer(models.LoadBalancerTargetServer{
                        Id:                   14,
                    }),
                    Targets:              []models.Target{
                        models.Target{
                            HealthStatus:         []models.HealthStatus{
                                models.HealthStatus{
                                    ListenPort:           models.ToPointer(142),
                                    Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                                },
                                models.HealthStatus{
                                    ListenPort:           models.ToPointer(142),
                                    Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                                },
                            },
                            Server:               models.ToPointer(models.Server11{
                                Id:                   14,
                            }),
                            Type:                 models.ToPointer("type2"),
                            UsePrivateIp:         models.ToPointer(false),
                        },
                        models.Target{
                            HealthStatus:         []models.HealthStatus{
                                models.HealthStatus{
                                    ListenPort:           models.ToPointer(142),
                                    Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                                },
                                models.HealthStatus{
                                    ListenPort:           models.ToPointer(142),
                                    Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                                },
                            },
                            Server:               models.ToPointer(models.Server11{
                                Id:                   14,
                            }),
                            Type:                 models.ToPointer("type2"),
                            UsePrivateIp:         models.ToPointer(false),
                        },
                        models.Target{
                            HealthStatus:         []models.HealthStatus{
                                models.HealthStatus{
                                    ListenPort:           models.ToPointer(142),
                                    Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                                },
                                models.HealthStatus{
                                    ListenPort:           models.ToPointer(142),
                                    Status:               models.ToPointer(models.Status30Enum_UNKNOWN),
                                },
                            },
                            Server:               models.ToPointer(models.Server11{
                                Id:                   14,
                            }),
                            Type:                 models.ToPointer("type2"),
                            UsePrivateIp:         models.ToPointer(false),
                        },
                    },
                    Type:                 models.Type29Enum_IP,
                },
            },
        },
    }

}
```



