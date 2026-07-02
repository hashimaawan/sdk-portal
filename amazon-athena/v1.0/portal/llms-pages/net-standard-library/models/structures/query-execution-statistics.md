# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.


# Class Name

`QueryExecutionStatistics`


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

QueryExecutionStatistics queryExecutionStatistics = new QueryExecutionStatistics
{
    EngineExecutionTimeInMillis = 98,
    DataScannedInBytes = 86,
    DataManifestLocation = "DataManifestLocation2",
    TotalExecutionTimeInMillis = 136,
    QueryQueueTimeInMillis = 142,
};
```



