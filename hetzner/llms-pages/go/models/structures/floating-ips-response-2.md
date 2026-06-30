# Floating Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMg


# Class Name

`FloatingIpsResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIp` | [`models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/floating-ip.md) | Required | - |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    floatingIpsResponse2 := models.FloatingIpsResponse2{
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



