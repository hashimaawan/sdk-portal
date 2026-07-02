# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.

*This model accepts additional fields of type object.*


# Class Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

FilterDefinition filterDefinition = new FilterDefinition
{
    Name = "Name2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



