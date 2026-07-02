# Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFByZXBhcmVkU3RhdGVtZW50T3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`GetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `PreparedStatement` | [`PreparedStatement1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/prepared-statement-1.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

GetPreparedStatementOutput getPreparedStatementOutput = new GetPreparedStatementOutput
{
    PreparedStatement = new PreparedStatement1
    {
        StatementName = "StatementName4",
        QueryStatement = "QueryStatement8",
        WorkGroupName = "WorkGroupName8",
        Description = "Description0",
        LastModifiedTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



