# Table Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlRhYmxlTWV0YWRhdGE

Contains metadata for a table.


# Class Name

`TableMetadata`


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

TableMetadata tableMetadata = new TableMetadata
{
    Name = "Name0",
    CreateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    LastAccessTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    TableType = "TableType4",
    Columns = new List<Column>
    {
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
        new Column
        {
            Name = "Name6",
            Type = "Type6",
            Comment = "Comment0",
        },
    },
};
```



