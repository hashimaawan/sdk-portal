# Update Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZVNlcnZlclJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`UpdateServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Optional | New name to set |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

UpdateServerRequest updateServerRequest = new UpdateServerRequest
{
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "my-server",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



