# Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXRpc3RpY3M


# Class Name

`Statistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `EngineExecutionTimeInMillis` | `int?` | Optional | - |
| `DataScannedInBytes` | `int?` | Optional | - |
| `DataManifestLocation` | `string` | Optional | - |
| `TotalExecutionTimeInMillis` | `int?` | Optional | - |
| `QueryQueueTimeInMillis` | `int?` | Optional | - |
| `QueryPlanningTimeInMillis` | `int?` | Optional | - |
| `ServiceProcessingTimeInMillis` | `int?` | Optional | - |
| `ResultReuseInformation` | [`ResultReuseInformation2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-reuse-information-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

Statistics statistics = new Statistics
{
    EngineExecutionTimeInMillis = 72,
    DataScannedInBytes = 60,
    DataManifestLocation = "DataManifestLocation0",
    TotalExecutionTimeInMillis = 146,
    QueryQueueTimeInMillis = 116,
};
```



