# Terminate Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`TerminateSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `SessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

TerminateSessionRequest terminateSessionRequest = new TerminateSessionRequest
{
    SessionId = "SessionId0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



