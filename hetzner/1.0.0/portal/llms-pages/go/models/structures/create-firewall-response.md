# Create Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkNyZWF0ZUZpcmV3YWxsUmVzcG9uc2U

*This model accepts additional fields of type interface{}.*


# Class Name

`CreateFirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Actions` | [`[]models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/action.md) | Optional | - |
| `Firewall` | [`*models.Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/firewall.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    createFirewallResponse := models.CreateFirewallResponse{
        Actions:               []models.Action{
            models.Action{
                Command:               "set_firewall_rules",
                Error:                 models.ToPointer(models.Error{
                    Code:                  "action_failed",
                    Message:               "Action failed",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Finished:              models.ToPointer("2016-01-30T23:56:00+00:00"),
                Id:                    13,
                Progress:              float64(100),
                Resources:             []models.Resource{
                    models.Resource{
                        Id:                    38,
                        Type:                  "firewall",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Started:               "2016-01-30T23:55:00+00:00",
                Status:                models.Status_Success,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.Action{
                Command:               "apply_firewall",
                Error:                 models.ToPointer(models.Error{
                    Code:                  "action_failed",
                    Message:               "Action failed",
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                }),
                Finished:              models.ToPointer("2016-01-30T23:56:00+00:00"),
                Id:                    14,
                Progress:              float64(100),
                Resources:             []models.Resource{
                    models.Resource{
                        Id:                    42,
                        Type:                  "server",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                    models.Resource{
                        Id:                    38,
                        Type:                  "firewall",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                Started:               "2016-01-30T23:55:00+00:00",
                Status:                models.Status_Success,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Firewall:              models.ToPointer(models.Firewall{
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
            Created:               "created6",
            Id:                    4,
            Labels:                map[string]string{
                "key0": "labels2",
                "key1": "labels1",
            },
            Name:                  "name6",
            Rules:                 []models.Rule{
                models.Rule{
                    Description:           models.NewOptional(models.ToPointer("description2")),
                    DestinationIps:        []string{
                        "destination_ips1",
                        "destination_ips2",
                        "destination_ips3",
                    },
                    Direction:             models.Direction_In,
                    Port:                  models.ToPointer("port8"),
                    Protocol:              models.Protocol_Udp,
                    SourceIps:             []string{
                        "source_ips1",
                        "source_ips2",
                        "source_ips3",
                    },
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
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



