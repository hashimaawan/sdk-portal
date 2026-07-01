# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0

*This model accepts additional fields of type object.*


# Class Name

`CreateFloatingIpRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Optional | - |
| `HomeLocation` | `string` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Optional | - |
| `Server` | `int?` | Optional | Server to assign the Floating IP to |
| `Type` | [`Type17`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-17.md) | Required | Floating IP type |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

CreateFloatingIpRequest createFloatingIpRequest = new CreateFloatingIpRequest
{
    Type = Type17.Ipv4,
    Description = "Web Frontend",
    HomeLocation = "fsn1",
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "Web Frontend",
    Server = 42,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



