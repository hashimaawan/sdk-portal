# Engine Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24

The Athena engine version for running queries, or the PySpark engine version for running sessions.

*This model accepts additional fields of type interface{}.*


# Class Name

`EngineVersion`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SelectedEngineVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `EffectiveEngineVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    engineVersion := models.EngineVersion{
        SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion0"),
        EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion0"),
        AdditionalProperties:   map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



