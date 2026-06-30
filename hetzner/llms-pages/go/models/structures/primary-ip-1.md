# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/go/x-redirect/JTI0bSUyRlByaW1hcnlJUDE


# Class Name

`PrimaryIP1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `*int` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all |
| `AssigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `AutoDelete` | `bool` | Required | Delete this Primary IP when the resource it is assigned to is deleted |
| `Blocked` | `bool` | Required | Whether the IP is blocked |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Datacenter` | [`models.Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at |
| `DnsPtr` | [`[]models.DnsPtr`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `Id` | `int` | Required | ID of the Resource |
| `Ip` | `string` | Required | IP address |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`models.Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Type` | [`models.Type50Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/go/models/enumerations/type-50.md) | Required | Type of the Primary IP |


# Example

```go
package main

import (
    "hetznercloudapi/models"
)

func main() {
    primaryIP1 := models.PrimaryIP1{
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
            "key0": "labels4",
            "key1": "labels3",
        },
        Name:                 "my-resource",
        Protection:           models.Protection{
            Delete:               false,
        },
        Type:                 models.Type50Enum_IPV4,
    }

}
```



