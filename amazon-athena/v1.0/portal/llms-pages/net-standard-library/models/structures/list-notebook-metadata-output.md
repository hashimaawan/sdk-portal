# List Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxpc3ROb3RlYm9va01ldGFkYXRhT3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`ListNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NextToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `NotebookMetadataList` | [`List<NotebookMetadata>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/notebook-metadata.md) | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Collections.Generic;
using System.Globalization;

ListNotebookMetadataOutput listNotebookMetadataOutput = new ListNotebookMetadataOutput
{
    NextToken = "NextToken2",
    NotebookMetadataList = new List<NotebookMetadata>
    {
        new NotebookMetadata
        {
            NotebookId = "NotebookId4",
            Name = "Name4",
            WorkGroup = "WorkGroup6",
            CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
                provider: CultureInfo.InvariantCulture,
                DateTimeStyles.RoundtripKind),
            Type = NotebookType1.Ipynb,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



