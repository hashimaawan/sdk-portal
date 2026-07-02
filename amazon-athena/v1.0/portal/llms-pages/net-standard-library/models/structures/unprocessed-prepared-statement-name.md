# Unprocessed Prepared Statement Name

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUHJlcGFyZWRTdGF0ZW1lbnROYW1l

The name of a prepared statement that could not be returned.

*This model accepts additional fields of type object.*


# Class Name

`UnprocessedPreparedStatementName`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatementName` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `ErrorCode` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `ErrorMessage` | `string` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

UnprocessedPreparedStatementName unprocessedPreparedStatementName = new UnprocessedPreparedStatementName
{
    StatementName = "StatementName8",
    ErrorCode = "ErrorCode6",
    ErrorMessage = "ErrorMessage6",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



