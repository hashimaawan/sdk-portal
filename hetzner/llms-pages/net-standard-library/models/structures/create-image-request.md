# Create Image Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZUltYWdlUmVxdWVzdA


# Class Name

`CreateImageRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Description` | `string` | Optional | Description of the Image, will be auto-generated if not set |
| `Labels` | [`Labels`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/structures/labels.md) | Optional | User-defined labels (key-value pairs) |
| `Type` | [`Type63Enum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/net-standard-library/models/enumerations/type-63.md) | Optional | Type of Image to create (default: `snapshot`) |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

CreateImageRequest createImageRequest = new CreateImageRequest
{
    Description = "my image",
    Labels = new Labels
    {
        Labelkey = "labelkey4",
    },
    Type = Type63Enum.Snapshot,
};
```



