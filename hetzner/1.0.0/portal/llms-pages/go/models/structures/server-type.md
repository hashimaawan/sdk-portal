# Server Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/go/x-redirect/JTI0bSUyRlNlcnZlclR5cGU

*This model accepts additional fields of type interface{}.*


# Class Name

`ServerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Cores` | `float64` | Required | Number of cpu cores a Server of this type will have |
| `CpuType` | [`models.CpuType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `Deprecated` | `bool` | Required | True if Server type is deprecated |
| `Description` | `string` | Required | Description of the Server type |
| `Disk` | `float64` | Required | Disk size a Server of this type will have in GB |
| `Id` | `float64` | Required | ID of the Server type |
| `Memory` | `float64` | Required | Memory a Server of this type will have in GB |
| `Name` | `string` | Required | Unique identifier of the Server type |
| `Prices` | [`[]models.Price9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/structures/price-9.md) | Required | Prices in different Locations |
| `StorageType` | [`models.StorageType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/go/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "hetznerCloudApi/models"
)

func main() {
    serverType := models.ServerType{
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
    }

}
```



