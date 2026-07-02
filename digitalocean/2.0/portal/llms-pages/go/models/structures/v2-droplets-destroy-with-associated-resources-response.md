# V2 Droplets Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`V2DropletsDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | [`[]models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/floating-ip.md) | Optional | - |
| `ReservedIps` | [`[]models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/floating-ip.md) | Optional | - |
| `Snapshots` | [`[]models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/floating-ip.md) | Optional | - |
| `VolumeSnapshots` | [`[]models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/floating-ip.md) | Optional | - |
| `Volumes` | [`[]models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/floating-ip.md) | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    v2DropletsDestroyWithAssociatedResourcesResponse := models.V2DropletsDestroyWithAssociatedResourcesResponse{
        FloatingIps:           []models.FloatingIp{
            models.FloatingIp{
                Cost:                  models.ToPointer("cost0"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.FloatingIp{
                Cost:                  models.ToPointer("cost0"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        ReservedIps:           []models.FloatingIp{
            models.FloatingIp{
                Cost:                  models.ToPointer("cost8"),
                Id:                    models.ToPointer("id0"),
                Name:                  models.ToPointer("name0"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Snapshots:             []models.FloatingIp{
            models.FloatingIp{
                Cost:                  models.ToPointer("cost0"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.FloatingIp{
                Cost:                  models.ToPointer("cost0"),
                Id:                    models.ToPointer("id2"),
                Name:                  models.ToPointer("name2"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        VolumeSnapshots:       []models.FloatingIp{
            models.FloatingIp{
                Cost:                  models.ToPointer("cost6"),
                Id:                    models.ToPointer("id8"),
                Name:                  models.ToPointer("name8"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Volumes:               []models.FloatingIp{
            models.FloatingIp{
                Cost:                  models.ToPointer("cost4"),
                Id:                    models.ToPointer("id6"),
                Name:                  models.ToPointer("name6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
            models.FloatingIp{
                Cost:                  models.ToPointer("cost4"),
                Id:                    models.ToPointer("id6"),
                Name:                  models.ToPointer("name6"),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



