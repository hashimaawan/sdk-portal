# Update Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZUltYWdlUmVxdWVzdA


# Class Name

`UpdateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Optional | New description of Image |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Type` | [`Type24Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/type-24.md) | Optional | Destination Image type to convert to |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;
using HetznerCloudAPI.Standard.Utilities;

UpdateImageRequest updateImageRequest = new UpdateImageRequest
{
    Description = "My new Image description",
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Type = Type24Enum.Snapshot,
};
```



