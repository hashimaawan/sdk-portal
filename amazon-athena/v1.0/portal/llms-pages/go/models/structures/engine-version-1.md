# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SelectedEngineVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `EffectiveEngineVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    engineVersion1 := models.EngineVersion1{
        SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion2"),
        EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion8"),
    }

}
```



