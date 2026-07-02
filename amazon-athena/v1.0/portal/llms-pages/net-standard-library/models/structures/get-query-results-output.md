# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `UpdateCount` | `int?` | Optional | - |
| `ResultSet` | [`ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/result-set-2.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Collections.Generic;

GetQueryResultsOutput getQueryResultsOutput = new GetQueryResultsOutput
{
    UpdateCount = 60,
    ResultSet = new ResultSet2
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
                    },
                    new Datum
                    {
                        VarCharValue = "VarCharValue8",
                    },
                },
            },
            new Row
            {
                Data = new List<Datum>
                {
                    new Datum
                    {
                        VarCharValue = "VarCharValue8",
                    },
                    new Datum
                    {
                        VarCharValue = "VarCharValue8",
                    },
                },
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
                },
            },
        },
    },
    NextToken = "NextToken0",
};
```



