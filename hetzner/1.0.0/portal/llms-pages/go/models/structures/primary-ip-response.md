# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl


# Class Name

`PrimaryIPResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PrimaryIp` | [`models.PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/primary-ip-1.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    primaryIPResponse := models.PrimaryIPResponse{
        PrimaryIp:            models.PrimaryIP1{
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
                "key1": "labels1",
            },
            Name:                 "my-resource",
            Protection:           models.Protection{
                Delete:               false,
            },
            Type:                 models.Type50Enum_IPV4,
        },
    }

}
```



