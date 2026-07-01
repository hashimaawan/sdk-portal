# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | New Volume name |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

UpdateVolumeRequest updateVolumeRequest = new UpdateVolumeRequest
{
    Name = "database-storage",
    Labels = new Labels2
    {
        Labelkey = "labelkey4",
        ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



