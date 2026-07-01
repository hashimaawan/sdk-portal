# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Blocked` | `bool` | Required | Whether the IP is blocked |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Description` | `*string` | Required | Description of the Resource |
| `DnsPtr` | [`[]models.DnsPtr`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `HomeLocation` | [`models.HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. |
| `Id` | `int` | Required | ID of the Resource |
| `Ip` | `string` | Required | IP address |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`models.Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Server` | `*int` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all |
| `Type` | [`models.Type16Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-16.md) | Required | Type of the Floating IP |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    floatingIp := models.FloatingIp{
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
            "key0": "labels6",
        },
        Name:                 "my-resource",
        Protection:           models.Protection{
            Delete:               false,
        },
        Server:               models.ToPointer(42),
        Type:                 models.Type16Enum_IPV4,
    }

}
```



