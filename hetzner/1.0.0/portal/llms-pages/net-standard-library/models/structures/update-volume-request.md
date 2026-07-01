# Update Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZVZvbHVtZVJlcXVlc3Q


# Class Name

`UpdateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Required | New Volume name |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

UpdateVolumeRequest updateVolumeRequest = new UpdateVolumeRequest
{
    Name = "database-storage",
    Labels = new Labels2
    {
        Labelkey = "labelkey4",
    },
};
```



