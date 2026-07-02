# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ

*This model accepts additional fields of type object.*


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `NamedQueryId` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

CreateNamedQueryOutput createNamedQueryOutput = new CreateNamedQueryOutput
{
    NamedQueryId = "NamedQueryId0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



