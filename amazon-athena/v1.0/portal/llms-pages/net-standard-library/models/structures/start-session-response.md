# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl

*This model accepts additional fields of type object.*


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `State` | [`SessionState1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/session-state-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

StartSessionResponse startSessionResponse = new StartSessionResponse
{
    SessionId = "SessionId4",
    State = SessionState1.Creating,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



