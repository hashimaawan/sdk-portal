# Calculation Statistics

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdGlzdGljcw

Contains statistics for a notebook calculation.


# Class Name

`CalculationStatistics`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `DpuExecutionInMillis` | `int?` | Optional | - |
| `Progress` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;

CalculationStatistics calculationStatistics = new CalculationStatistics
{
    DpuExecutionInMillis = 248,
    Progress = "Progress8",
};
```



