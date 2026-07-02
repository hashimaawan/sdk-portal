# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `StateFilter` | [`SessionState3Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/session-state-3.md) | Optional | - |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```csharp
using AmazonAthena.Standard.Models;

ListSessionsRequest listSessionsRequest = new ListSessionsRequest
{
    WorkGroup = "WorkGroup8",
    StateFilter = SessionState3Enum.CREATING,
    MaxResults = 100,
    NextToken = "NextToken6",
};
```



