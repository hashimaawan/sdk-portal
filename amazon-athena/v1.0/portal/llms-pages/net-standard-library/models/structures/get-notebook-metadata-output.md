# Get Notebook Metadata Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkdldE5vdGVib29rTWV0YWRhdGFPdXRwdXQ


# Class Name

`GetNotebookMetadataOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookMetadata` | [`NotebookMetadata1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/structures/notebook-metadata-1.md) | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using System.Globalization;

GetNotebookMetadataOutput getNotebookMetadataOutput = new GetNotebookMetadataOutput
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
};
```



