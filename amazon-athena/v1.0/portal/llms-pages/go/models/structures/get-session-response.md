# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type interface{}.*


# Class Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `WorkGroup` | `*string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `EngineConfiguration` | [`*models.EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-configuration-1.md) | Optional | - |
| `NotebookVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SessionConfiguration` | [`*models.SessionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/session-configuration-2.md) | Optional | - |
| `Status` | [`*models.Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/status-3.md) | Optional | - |
| `Statistics` | [`*models.Statistics3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/statistics-3.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    getSessionResponse := models.GetSessionResponse{
        SessionId:             models.ToPointer("SessionId6"),
        Description:           models.ToPointer("Description4"),
        WorkGroup:             models.ToPointer("WorkGroup4"),
        EngineVersion:         models.ToPointer("EngineVersion8"),
        EngineConfiguration:   models.ToPointer(models.EngineConfiguration1{
            CoordinatorDpuSize:     models.ToPointer(1),
            MaxConcurrentDpus:      94,
            DefaultExecutorDpuSize: models.ToPointer(1),
            AdditionalConfigs:      models.ToPointer(models.AdditionalConfigs{
                AdditionalProperties:  map[string]string{
                    "exampleAdditionalProperty": "AdditionalConfigs_additionalProperties5",
                },
            }),
            AdditionalProperties:   map[string]interface{}{
                "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
            },
        }),
        AdditionalProperties:  map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



