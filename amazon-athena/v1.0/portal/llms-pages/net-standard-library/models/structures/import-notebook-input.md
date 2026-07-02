# Import Notebook Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkltcG9ydE5vdGVib29rSW5wdXQ

*This model accepts additional fields of type object.*


# Class Name

`ImportNotebookInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `WorkGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `Payload` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `10485760` |
| `Type` | [`NotebookType2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/net-standard-library/models/enumerations/notebook-type-2.md) | Required | - |
| `ClientRequestToken` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36`, *Pattern*: `[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

ImportNotebookInput importNotebookInput = new ImportNotebookInput
{
    WorkGroup = "WorkGroup2",
    Name = "Name0",
    Payload = "Payload6",
    Type = NotebookType2.Ipynb,
    ClientRequestToken = "ClientRequestToken4",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



