# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ExecutorStateFilter` | [`ExecutorState1Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/executor-state-1.md) | Optional | - |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListExecutorsRequest listExecutorsRequest = new ListExecutorsRequest
{
    SessionId = "SessionId0",
    ExecutorStateFilter = ExecutorState1Enum.CREATING,
    MaxResults = 100,
    NextToken = "NextToken8",
};
```



