# Update Primary IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZVByaW1hcnlJUFJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`UpdatePrimaryIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `AutoDelete` | `bool?` | Optional | Delete this Primary IP when the resource it is assigned to is deleted |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Optional | New unique name to set |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

UpdatePrimaryIpRequest updatePrimaryIpRequest = new UpdatePrimaryIpRequest
{
    AutoDelete = true,
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "my-ip",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



