# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/net-standard-library/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type object.*


# Class Name

`Patch`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Op` | [`Op`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/net-standard-library/models/enumerations/op.md) | Required | - |
| `Path` | `string` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute |
| `MValue` | `object` | Optional | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using M1PasswordConnect.Standard.Models;
using M1PasswordConnect.Standard.Utilities;

Patch patch = new Patch
{
    Op = Op.Remove,
    Path = "/fields/06gnn2b95example10q91512p5/label",
    MValue = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



