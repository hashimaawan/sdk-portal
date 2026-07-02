# List Table Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3RUYWJsZU1ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`ListTableMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `TableMetadataList` | [`List<TableMetadata>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/table-metadata.md) | Optional | - |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            PartitionKeys = new List<Column>
            {
                new Column
                {
                    Name = "Name6",
                    Type = "Type6",
                    Comment = "Comment0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Column
                {
                    Name = "Name6",
                    Type = "Type6",
                    Comment = "Comment0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Column
                {
                    Name = "Name6",
                    Type = "Type6",
                    Comment = "Comment0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
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
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            PartitionKeys = new List<Column>
            {
                new Column
                {
                    Name = "Name6",
                    Type = "Type6",
                    Comment = "Comment0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Column
                {
                    Name = "Name6",
                    Type = "Type6",
                    Comment = "Comment0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
                new Column
                {
                    Name = "Name6",
                    Type = "Type6",
                    Comment = "Comment0",
                    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
                },
            },
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    NextToken = "NextToken0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



