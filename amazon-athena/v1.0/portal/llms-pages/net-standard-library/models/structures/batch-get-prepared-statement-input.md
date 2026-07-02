# Batch Get Prepared Statement Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRJbnB1dA


# Class Name

`BatchGetPreparedStatementInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreparedStatementNames` | `List<string>` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

BatchGetPreparedStatementInput batchGetPreparedStatementInput = new BatchGetPreparedStatementInput
{
    PreparedStatementNames = new List<string>
    {
        "PreparedStatementNames8",
        "PreparedStatementNames9",
        "PreparedStatementNames0",
    },
    WorkGroup = "WorkGroup6",
};
```



