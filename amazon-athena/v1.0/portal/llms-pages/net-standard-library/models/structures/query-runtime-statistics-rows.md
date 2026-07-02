# Query Runtime Statistics Rows

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlF1ZXJ5UnVudGltZVN0YXRpc3RpY3NSb3dz

Statistics such as input rows and bytes read by the query, rows and bytes output by the query, and the number of rows written by the query.


# Class Name

`QueryRuntimeStatisticsRows`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `InputRows` | `int?` | Optional | - |
| `InputBytes` | `int?` | Optional | - |
| `OutputBytes` | `int?` | Optional | - |
| `OutputRows` | `int?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;

QueryRuntimeStatisticsRows queryRuntimeStatisticsRows = new QueryRuntimeStatisticsRows
{
    InputRows = 234,
    InputBytes = 254,
    OutputBytes = 40,
    OutputRows = 226,
};
```



