# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/go/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


# Class Name

`Statistics`


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


# Example

```go
package main

import (
    "amazonathena/models"
)

func main() {
    statistics := models.Statistics{
        EngineExecutionTimeInMillis:   models.ToPointer(72),
        DataScannedInBytes:            models.ToPointer(60),
        DataManifestLocation:          models.ToPointer("DataManifestLocation0"),
        TotalExecutionTimeInMillis:    models.ToPointer(146),
        QueryQueueTimeInMillis:        models.ToPointer(116),
    }

}
```



