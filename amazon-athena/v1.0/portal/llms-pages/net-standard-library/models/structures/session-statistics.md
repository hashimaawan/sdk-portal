# Session Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0aXN0aWNz

Contains statistics for a session.


# Class Name

`SessionStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `int?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

SessionStatistics sessionStatistics = new SessionStatistics
{
    DpuExecutionInMillis = 188,
};
```



