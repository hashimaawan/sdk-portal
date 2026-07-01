# Label Selector 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxhYmVsU2VsZWN0b3Ix

Configuration for type LabelSelector, required if type is `label_selector`

*This model accepts additional fields of type object.*


# Class Name

`LabelSelector1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Selector` | `string` | Required | Label selector |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

LabelSelector1 labelSelector1 = new LabelSelector1
{
    Selector = "selector2",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



