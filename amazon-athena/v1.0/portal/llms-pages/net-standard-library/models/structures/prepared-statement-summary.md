# Prepared Statement Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlByZXBhcmVkU3RhdGVtZW50U3VtbWFyeQ

The name and last modified time of the prepared statement.


# Class Name

`PreparedStatementSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `StatementName` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256`, *Pattern*: `[a-zA-Z_][a-zA-Z0-9_@:]{1,256}` |
| `LastModifiedTime` | `DateTime?` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Globalization;

PreparedStatementSummary preparedStatementSummary = new PreparedStatementSummary
{
    StatementName = "StatementName4",
    LastModifiedTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
};
```



