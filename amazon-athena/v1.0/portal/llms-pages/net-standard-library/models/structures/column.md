# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type object.*


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `Type` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` |
| `Comment` | `string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using AmazonAthena.Standard.Models;
using AmazonAthena.Standard.Utilities;

Column column = new Column
{
    Name = "Name6",
    Type = "Type6",
    Comment = "Comment2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



