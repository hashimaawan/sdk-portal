# Label Selector

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3I

*This model accepts additional fields of type object.*


# Class Name

`LabelSelector`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Selector` | `string` | Required | Label selector |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LabelSelector labelSelector = new LabelSelector
{
    Selector = "env=prod",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



