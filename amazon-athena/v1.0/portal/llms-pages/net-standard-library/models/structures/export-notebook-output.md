# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0

*This model accepts additional fields of type object.*


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookMetadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/notebook-metadata-1.md) | Optional | - |
| `Payload` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

ExportNotebookOutput exportNotebookOutput = new ExportNotebookOutput
{
    NotebookMetadata = new NotebookMetadata1
    {
        NotebookId = "NotebookId0",
        Name = "Name0",
        WorkGroup = "WorkGroup2",
        CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
            provider: CultureInfo.InvariantCulture,
            DateTimeStyles.RoundtripKind),
        Type = NotebookType1.Ipynb,
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    Payload = "Payload2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



