# Server Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlciUyNTIwVHlwZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type interface{}.*


# Class Name

`ServerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ServerTypes` | [`[]models.ServerTypes7`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/server-types-7.md) | Required | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serverTypesResponse := models.ServerTypesResponse{
        ServerTypes:           []models.ServerTypes7{
            models.ServerTypes7{
                Cores:                 float64(1),
                CpuType:               models.CpuType_Shared,
                Deprecated:            false,
                Description:           "CX11",
                Disk:                  float64(24),
                Id:                    float64(1),
                Memory:                float64(1),
                Name:                  "cx11",
                Prices:                []models.Price9{
                    models.Price9{
                        Location:              "fsn1",
                        PriceHourly:           models.PriceHourly8{
                            Gross:                 "1.1900000000000000",
                            Net:                   "1.0000000000",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        PriceMonthly:          models.PriceMonthly10{
                            Gross:                 "1.1900000000000000",
                            Net:                   "1.0000000000",
                            AdditionalProperties:  map[string]interface{}{
                                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                            },
                        },
                        AdditionalProperties:  map[string]interface{}{
                            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                        },
                    },
                },
                StorageType:           models.StorageType_Local,
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



