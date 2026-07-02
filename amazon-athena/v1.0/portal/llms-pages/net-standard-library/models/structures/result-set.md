# Result Set

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlc3VsdFNldA

The metadata and rows that make up a query result set. The metadata describes the column structure and data types. To return a <code>ResultSet</code> object, use <a>GetQueryResults</a>.

*This model accepts additional fields of type object.*


# Class Name

`ResultSet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Rows` | [`List<Row>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/row.md) | Optional | - |
| `ResultSetMetadata` | [`ResultSetMetadata2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-set-metadata-2.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;

ResultSet resultSet = new ResultSet
{
    Rows = new List<Row>
    {
        new Row
        {
            Data = new List<Datum>
            {
                new Datum
                {
                    VarCharValue = "VarCharValue8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Datum
                {
                    VarCharValue = "VarCharValue8",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ResultSetMetadata = new ResultSetMetadata2
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
                ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
            },
        },
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



