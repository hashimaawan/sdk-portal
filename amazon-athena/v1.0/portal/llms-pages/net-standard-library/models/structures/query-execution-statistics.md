# Query Execution Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdGlzdGljcw

The amount of data scanned during the query execution and the amount of time that it took to execute, and the type of statement that was run.

*This model accepts additional fields of type object.*


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
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

QueryExecutionStatistics queryExecutionStatistics = new QueryExecutionStatistics
{
    EngineExecutionTimeInMillis = 98,
    DataScannedInBytes = 86,
    DataManifestLocation = "DataManifestLocation2",
    TotalExecutionTimeInMillis = 136,
    QueryQueueTimeInMillis = 142,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



