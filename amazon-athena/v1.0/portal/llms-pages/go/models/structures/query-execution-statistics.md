# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.

*This model accepts additional fields of type interface{}.*


# Class Name

`QueryExecutionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EngineExecutionTimeInMillis` | `*int` | Optional | - |
| `DataScannedInBytes` | `*int` | Optional | - |
| `DataManifestLocation` | `*string` | Optional | - |
| `TotalExecutionTimeInMillis` | `*int` | Optional | - |
| `QueryQueueTimeInMillis` | `*int` | Optional | - |
| `QueryPlanningTimeInMillis` | `*int` | Optional | - |
| `ServiceProcessingTimeInMillis` | `*int` | Optional | - |
| `ResultReuseInformation` | [`*models.ResultReuseInformation2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/go/models/structures/result-reuse-information-2.md) | Optional | - |
| `AdditionalProperties` | `map[string]interface{}` | Optional | - |


# Example

```go
package main

import (
    "amazonAthena/models"
)

func main() {
    queryExecutionStatistics := models.QueryExecutionStatistics{
        EngineExecutionTimeInMillis:   models.ToPointer(98),
        DataScannedInBytes:            models.ToPointer(86),
        DataManifestLocation:          models.ToPointer("DataManifestLocation2"),
        TotalExecutionTimeInMillis:    models.ToPointer(136),
        QueryQueueTimeInMillis:        models.ToPointer(142),
        AdditionalProperties:          map[string]interface{}{
            "exampleAdditionalProperty": interface{}("[key1, val1][key2, val2]"),
        },
    }

}
```



