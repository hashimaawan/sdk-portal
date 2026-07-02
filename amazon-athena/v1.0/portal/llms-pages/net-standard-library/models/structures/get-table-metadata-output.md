# Get Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFRhYmxlTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TableMetadata` | [`TableMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/table-metadata-2.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;
using System.Globalization;

GetTableMetadataOutput getTableMetadataOutput = new GetTableMetadataOutput
{
    TableMetadata = new TableMetadata2
    {
        Name = "Name6",
        CreateTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        LastAccessTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        TableType = "TableType0",
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
        },
    },
};
```



