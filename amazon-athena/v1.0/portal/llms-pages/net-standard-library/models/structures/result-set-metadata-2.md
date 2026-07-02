# Result Set Metadata 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRhMg


# Class Name

`ResultSetMetadata2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ColumnInfo` | [`List<ColumnInfo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/column-info.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ResultSetMetadata2 resultSetMetadata2 = new ResultSetMetadata2
{
    ColumnInfo = new List<ColumnInfo>
    {
        new ColumnInfo
        {
            Name = "Name6",
            Type = "Type6",
            CatalogName = "CatalogName0",
            SchemaName = "SchemaName0",
            TableName = "TableName2",
            Label = "Label4",
            Precision = 48,
        },
        new ColumnInfo
        {
            Name = "Name6",
            Type = "Type6",
            CatalogName = "CatalogName0",
            SchemaName = "SchemaName0",
            TableName = "TableName2",
            Label = "Label4",
            Precision = 48,
        },
    },
};
```



