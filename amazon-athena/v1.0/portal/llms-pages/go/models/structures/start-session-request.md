# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q

*This model accepts additional fields of type interface{}.*


# Class Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `EngineConfiguration` | [`models.EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/engine-configuration-1.md) | Required | - |
| `NotebookVersion` | `*string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `SessionIdleTimeoutInMinutes` | `*int` | Optional | **Constraints**: `>= 1`, `<= 480` |
| `ClientRequestToken` | `*string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    startSessionRequest := models.StartSessionRequest{
        Description:                 models.ToPointer("Description4"),
        WorkGroup:                   "WorkGroup2",
        EngineConfiguration:         models.EngineConfiguration1{
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
        },
        NotebookVersion:             models.ToPointer("NotebookVersion4"),
        SessionIdleTimeoutInMinutes: models.ToPointer(172),
        ClientRequestToken:          models.ToPointer("ClientRequestToken4"),
        AdditionalProperties:        map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



