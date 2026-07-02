# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/go/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type [interface{}](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md).*


# Class Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `CpuType` | [`*models.MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `"UNSPECIFIED"` |
| `Cpus` | `*string` | Optional | - |
| `MemoryBytes` | `*string` | Optional | - |
| `Name` | `*string` | Optional | - |
| `Slug` | `*string` | Optional | - |
| `TierDowngradeTo` | `*string` | Optional | - |
| `TierSlug` | `*string` | Optional | - |
| `TierUpgradeTo` | `*string` | Optional | - |
| `UsdPerMonth` | `*string` | Optional | - |
| `UsdPerSecond` | `*string` | Optional | - |
| `AdditionalProperties` | [`map[string]interface{}`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/go/models/structures/object.md) | Optional | - |


# Example

```go
package main

import (
    "digitalOceanApi/models"
)

func main() {
    instanceSize := models.InstanceSize{
        CpuType:               models.ToPointer(models.MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores_Shared),
        Cpus:                  models.ToPointer("3"),
        MemoryBytes:           models.ToPointer("1048"),
        Name:                  models.ToPointer("name"),
        Slug:                  models.ToPointer("basic"),
        TierDowngradeTo:       models.ToPointer("basic"),
        TierSlug:              models.ToPointer("basic"),
        TierUpgradeTo:         models.ToPointer("basic"),
        UsdPerMonth:           models.ToPointer("23"),
        UsdPerSecond:          models.ToPointer("0.00000001232"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



