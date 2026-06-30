# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ


# Class Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Action` | [`*models.Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/action.md) | Optional | - |
| `FloatingIp` | [`models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/floating-ip.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    floatingIpsResponse1 := models.FloatingIpsResponse1{
        Action:               models.ToPointer(models.Action{
            Command:              "command6",
            Error:                models.ToPointer(models.Error{
                Code:                 "code2",
                Message:              "message4",
            }),
            Finished:             models.ToPointer("finished0"),
            Id:                   238,
            Progress:             float64(143.26),
            Resources:            []models.Resource{
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
                models.Resource{
                    Id:                   198,
                    Type:                 "type0",
                },
            },
            Started:              "started8",
            Status:               models.StatusEnum_RUNNING,
        }),
        FloatingIp:           models.FloatingIp{
            Blocked:              false,
            Created:              "2016-01-30T23:55:00+00:00",
            Description:          models.ToPointer("this describes my resource"),
            DnsPtr:               []models.DnsPtr{
                models.DnsPtr{
                    DnsPtr:               "server.example.com",
                    Ip:                   "2001:db8::1",
                },
            },
            HomeLocation:         models.HomeLocation{
                City:                 "Falkenstein",
                Country:              "DE",
                Description:          "Falkenstein DC Park 1",
                Id:                   float64(1),
                Latitude:             float64(50.47612),
                Longitude:            float64(12.370071),
                Name:                 "fsn1",
                NetworkZone:          "eu-central",
            },
            Id:                   42,
            Ip:                   "131.232.99.1",
            Labels:               map[string]string{
                "key0": "labels4",
                "key1": "labels3",
                "key2": "labels2",
            },
            Name:                 "my-resource",
            Protection:           models.Protection{
                Delete:               false,
            },
            Server:               models.ToPointer(42),
            Type:                 models.Type16Enum_IPV4,
        },
    }

}
```



