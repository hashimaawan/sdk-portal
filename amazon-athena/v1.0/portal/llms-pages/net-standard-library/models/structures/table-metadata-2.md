# Table Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGEy


# Class Name

`TableMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `CreateTime` | `DateTime?` | Optional | - |
| `LastAccessTime` | `DateTime?` | Optional | - |
| `TableType` | `string` | Optional | **Constraints**: *Maximum Length*: `255` |
| `Columns` | [`List<Column>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/column.md) | Optional | - |
| `PartitionKeys` | [`List<Column>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/column.md) | Optional | - |
| `Parameters` | [`Parameters`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/parameters.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

TableMetadata2 tableMetadata2 = new TableMetadata2
{
    Name = "Name8",
    CreateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    LastAccessTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    TableType = "TableType6",
    Columns = new List<Column>
    {
        new Column
        {
            Name = "Name0",
            Type = "Type0",
            Comment = "Comment4",
        },
        new Column
        {
            Name = "Name0",
            Type = "Type0",
            Comment = "Comment4",
        },
    },
    PartitionKeys = new List<Column>
    {
        new Column
        {
            Name = "Name6",
            Type = "Type6",
            Comment = "Comment0",
        },
        new Column
        {
            Name = "Name6",
            Type = "Type6",
            Comment = "Comment0",
        },
    },
};
```



