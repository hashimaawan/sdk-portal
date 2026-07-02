# Batch Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25JbnB1dA

Contains an array of query execution IDs.


# Class Name

`BatchGetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `QueryExecutionIds` | `List<string>` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

BatchGetQueryExecutionInput batchGetQueryExecutionInput = new BatchGetQueryExecutionInput
{
    QueryExecutionIds = new List<string>
    {
        "QueryExecutionIds7",
        "QueryExecutionIds8",
        "QueryExecutionIds9",
    },
};
```



