# Engine Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24

Contains data processing unit (DPU) configuration settings and parameter mappings for a notebook engine.


# Class Name

`EngineConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CoordinatorDpuSize` | `*int` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `MaxConcurrentDpus` | `int` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `DefaultExecutorDpuSize` | `*int` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `AdditionalConfigs` | [`*models.AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/additional-configs.md) | Optional | - |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    engineConfiguration := models.EngineConfiguration{
        CoordinatorDpuSize:     models.ToPointer(1),
        MaxConcurrentDpus:      194,
        DefaultExecutorDpuSize: models.ToPointer(1),
        AdditionalConfigs:      models.ToPointer(models.AdditionalConfigs{
        }),
    }

}
```



