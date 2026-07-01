# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlByaW1hcnlJUDE

*This model accepts additional fields of type interface{}.*


# Class Name

`PrimaryIp1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AssigneeId` | `*int` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all |
| `AssigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `"server"` |
| `AutoDelete` | `bool` | Required | Delete this Primary IP when the resource it is assigned to is deleted |
| `Blocked` | `bool` | Required | Whether the IP is blocked |
| `Created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `Datacenter` | [`models.Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at |
| `DnsPtr` | [`[]models.DnsPtr`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `Id` | `int` | Required | ID of the Resource |
| `Ip` | `string` | Required | IP address |
| `Labels` | `map[string]string` | Required | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `Protection` | [`models.Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `Type` | [`models.Type50`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/type-50.md) | Required | Type of the Primary IP |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    primaryIp1 := models.PrimaryIp1{
        AssigneeId:            models.ToPointer(17),
        AssigneeType:          "server",
        AutoDelete:            true,
        Blocked:               false,
        Created:               "2016-01-30T23:55:00+00:00",
        Datacenter:            models.Datacenter2{
            Description:           "Falkenstein DC Park 8",
            Id:                    42,
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
            Name:                  "fsn1-dc8",
            ServerTypes:           models.ServerTypes{
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
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        DnsPtr:                []models.DnsPtr{
            models.DnsPtr{
                DnsPtr:                "server.example.com",
                Ip:                    "2001:db8::1",
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Id:                    42,
        Ip:                    "131.232.99.1",
        Labels:                map[string]string{
            "key0": "labels0",
        },
        Name:                  "my-resource",
        Protection:            models.Protection{
            Delete:                false,
            AdditionalProperties:  map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        },
        Type:                  models.Type50_Ipv4,
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



