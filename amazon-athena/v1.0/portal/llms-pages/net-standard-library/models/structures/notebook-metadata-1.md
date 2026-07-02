# Notebook Metadata 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRk5vdGVib29rTWV0YWRhdGEx

*This model accepts additional fields of type object.*


# Class Name

`NotebookMetadata1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NotebookId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `Name` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `WorkGroup` | `string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `CreationTime` | `DateTime?` | Optional | - |
| `Type` | [`NotebookType1?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/notebook-type-1.md) | Optional | - |
| `LastModifiedTime` | `DateTime?` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;
using System.Globalization;

NotebookMetadata1 notebookMetadata1 = new NotebookMetadata1
{
    NotebookId = "NotebookId2",
    Name = "Name2",
    WorkGroup = "WorkGroup4",
    CreationTime = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Type = NotebookType1.Ipynb,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



