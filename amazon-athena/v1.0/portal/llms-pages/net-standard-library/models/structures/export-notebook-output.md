# Export Notebook Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkV4cG9ydE5vdGVib29rT3V0cHV0


# Class Name

`ExportNotebookOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookMetadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/notebook-metadata-1.md) | Optional | - |
| `Payload` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |


# Example

```csharp
using AmazonAthena.Standard.Models;
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
        Type = NotebookType1Enum.IPYNB,
    },
    Payload = "Payload2",
};
```



