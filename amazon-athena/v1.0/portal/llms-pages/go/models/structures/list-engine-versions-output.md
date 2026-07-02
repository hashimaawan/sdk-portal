# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA

*This model accepts additional fields of type interface{}.*


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EngineVersions` | [`[]models.EngineVersion`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `NextToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    listEngineVersionsOutput := models.ListEngineVersionsOutput{
        EngineVersions:        []models.EngineVersion{
            models.EngineVersion{
                SelectedEngineVersion:  models.ToPointer("SelectedEngineVersion2"),
                EffectiveEngineVersion: models.ToPointer("EffectiveEngineVersion2"),
                AdditionalProperties:   map[string]interface{}{
                    "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
                },
            },
        },
        NextToken:             models.ToPointer("NextToken0"),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



