# Create Floating IP Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUZsb2F0aW5nSVBSZXF1ZXN0


# Class Name

`CreateFloatingIPRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Optional | - |
| `HomeLocation` | `string` | Optional | Home Location (routing is optimized for that Location). Only optional if Server argument is passed. |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Optional | - |
| `Server` | `int?` | Optional | Server to assign the Floating IP to |
| `Type` | [`Type17Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-17.md) | Required | Floating IP type |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;

CreateFloatingIPRequest createFloatingIPRequest = new CreateFloatingIPRequest
{
    Type = Type17Enum.Ipv4,
    Description = "Web Frontend",
    HomeLocation = "fsn1",
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Name = "Web Frontend",
    Server = 42,
};
```



