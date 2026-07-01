# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`[]models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `Firewall` | [`*models.Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall.md) | Optional | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    createFirewallResponse := models.CreateFirewallResponse{
        Actions:              []models.Action{
            models.Action{
                Command:              "set_firewall_rules",
                Error:                models.ToPointer(models.Error{
                    Code:                 "action_failed",
                    Message:              "Action failed",
                }),
                Finished:             models.ToPointer("2016-01-30T23:56:00+00:00"),
                Id:                   13,
                Progress:             float64(100),
                Resources:            []models.Resource{
                    models.Resource{
                        Id:                   38,
                        Type:                 "firewall",
                    },
                },
                Started:              "2016-01-30T23:55:00+00:00",
                Status:               models.StatusEnum_SUCCESS,
            },
            models.Action{
                Command:              "apply_firewall",
                Error:                models.ToPointer(models.Error{
                    Code:                 "action_failed",
                    Message:              "Action failed",
                }),
                Finished:             models.ToPointer("2016-01-30T23:56:00+00:00"),
                Id:                   14,
                Progress:             float64(100),
                Resources:            []models.Resource{
                    models.Resource{
                        Id:                   42,
                        Type:                 "server",
                    },
                    models.Resource{
                        Id:                   38,
                        Type:                 "firewall",
                    },
                },
                Started:              "2016-01-30T23:55:00+00:00",
                Status:               models.StatusEnum_SUCCESS,
            },
        },
        Firewall:             models.ToPointer(models.Firewall{
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
            Created:              "created6",
            Id:                   4,
            Labels:               map[string]string{
                "key0": "labels2",
                "key1": "labels1",
            },
            Name:                 "name6",
            Rules:                []models.Rule{
                models.Rule{
                    Description:          models.NewOptional(models.ToPointer("description2")),
                    DestinationIps:       []string{
                        "destination_ips1",
                        "destination_ips2",
                        "destination_ips3",
                    },
                    Direction:            models.DirectionEnum_IN,
                    Port:                 models.ToPointer("port8"),
                    Protocol:             models.ProtocolEnum_UDP,
                    SourceIps:            []string{
                        "source_ips1",
                        "source_ips2",
                        "source_ips3",
                    },
                },
            },
        }),
    }

}
```



