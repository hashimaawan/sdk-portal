# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type interface{}.*


# Class Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CoordinatorDpuSize` | `*int` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `MaxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `DefaultExecutorDpuSize` | `*int` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `AdditionalConfigs` | [`*models.AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/additional-configs.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    engineConfiguration1 := models.EngineConfiguration1{
        CoordinatorDpuSize:     models.ToPointer(1),
        MaxConcurrentDpus:      214,
        DefaultExecutorDpuSize: models.ToPointer(1),
        AdditionalConfigs:      models.ToPointer(models.AdditionalConfigs{
            AdditionalProperties:  map[string]string{
                "exampleAdditionalProperty": "AdditionalConfigs_additionalProperties5",
            },
        }),
        AdditionalProperties:   map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



