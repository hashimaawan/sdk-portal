# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TableMetadataList` | [`List<TableMetadata>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/table-metadata.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

ListTableMetadataOutput listTableMetadataOutput = new ListTableMetadataOutput
{
    TableMetadataList = new List<TableMetadata>
    {
        new TableMetadata
        {
            Name = "Name2",
            CreateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            LastAccessTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            TableType = "TableType2",
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
        },
        new TableMetadata
        {
            Name = "Name2",
            CreateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            LastAccessTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            TableType = "TableType2",
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
        },
    },
    NextToken = "NextToken0",
};
```



