# Result Set Metadata

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFNldE1ldGFkYXRh

The metadata that describes the column structure and data types of a table of query results. To return a <code>ResultSetMetadata</code> object, use <a>GetQueryResults</a>.


# Class Name

`ResultSetMetadata`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ColumnInfo` | [`List<ColumnInfo>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/column-info.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

ResultSetMetadata resultSetMetadata = new ResultSetMetadata
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



