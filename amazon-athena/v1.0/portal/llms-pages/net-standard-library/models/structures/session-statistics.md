# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.

*This model accepts additional fields of type object.*


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `int?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

SessionStatistics sessionStatistics = new SessionStatistics
{
    DpuExecutionInMillis = 188,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



