# Labels

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxhYmVscw

User-defined labels (key-value pairs)

*This model accepts additional fields of type object.*


# Class Name

`Labels`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labelkey` | `string` | Optional | New label |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Labels labels = new Labels
{
    Labelkey = "value",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



