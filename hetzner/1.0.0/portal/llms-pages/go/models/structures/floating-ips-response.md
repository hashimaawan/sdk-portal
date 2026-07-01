# Floating Ips Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`FloatingIpsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FloatingIps` | [`[]models.FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/floating-ip.md) | Required | - |
| `Meta` | [`*models.Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/meta.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    floatingIpsResponse := models.FloatingIpsResponse{
        FloatingIps:           []models.FloatingIp{
            models.FloatingIp{
                Blocked:               false,
                Created:               "2016-01-30T23:55:00+00:00",
                Description:           models.ToPointer("this describes my resource"),
                DnsPtr:                []models.DnsPtr{
                    models.DnsPtr{
                        DnsPtr:                "server.example.com",
                        Ip:                    "2001:db8::1",
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                HomeLocation:          models.HomeLocation{
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
                Id:                    42,
                Ip:                    "131.232.99.1",
                Labels:                map[string]string{
                    "key0": "labels2",
                },
                Name:                  "my-resource",
                Protection:            models.Protection{
                    Delete:                false,
                    AdditionalProperties:  map[string]interface{}{
                        "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                    },
                },
                Server:                models.ToPointer(42),
                Type:                  models.Type16_Ipv4,
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        Meta:                  models.ToPointer(models.Meta{
            Pagination:            models.Pagination{
                LastPage:              models.ToPointer(float64(77.7)),
                NextPage:              models.ToPointer(float64(209.18)),
                Page:                  float64(17.58),
                PerPage:               float64(13.34),
                PreviousPage:          models.ToPointer(float64(50.02)),
                TotalEntries:          models.ToPointer(float64(206.64)),
                AdditionalProperties:  map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
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



