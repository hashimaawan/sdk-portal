# Firewall Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVzcG9uc2U


# Class Name

`FirewallResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Firewall` | [`models.Firewall`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/firewall.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    firewallResponse := models.FirewallResponse{
        Firewall:             models.Firewall{
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
                "key0": "labels2",
                "key1": "labels1",
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
    }

}
```



