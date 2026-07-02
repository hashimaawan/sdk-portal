# Unprocessed Named Query Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkTmFtZWRRdWVyeUlk

Information about a named query ID that could not be processed.

*This model accepts additional fields of type object.*


# Class Name

`UnprocessedNamedQueryId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `ErrorCode` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ErrorMessage` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

UnprocessedNamedQueryId unprocessedNamedQueryId = new UnprocessedNamedQueryId
{
    NamedQueryId = "NamedQueryId0",
    ErrorCode = "ErrorCode8",
    ErrorMessage = "ErrorMessage8",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



