# Prepared Statement 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50MQ

*This model accepts additional fields of type object.*


# Class Name

`PreparedStatement1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatementName` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `QueryStatement` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `WorkGroupName` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Description` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `LastModifiedTime` | `DateTime?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

PreparedStatement1 preparedStatement1 = new PreparedStatement1
{
    StatementName = "StatementName6",
    QueryStatement = "QueryStatement0",
    WorkGroupName = "WorkGroupName0",
    Description = "Description8",
    LastModifiedTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



