# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `StateFilter` | [`SessionState3?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/session-state-3.md) | Optional | - |
| `MaxResults` | `int?` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `NextToken` | `string` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ListSessionsRequest listSessionsRequest = new ListSessionsRequest
{
    WorkGroup = "WorkGroup8",
    StateFilter = SessionState3.Creating,
    MaxResults = 100,
    NextToken = "NextToken6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



