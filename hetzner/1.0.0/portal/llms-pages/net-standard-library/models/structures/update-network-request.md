# Update Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlVwZGF0ZU5ldHdvcmtSZXF1ZXN0


# Class Name

`UpdateNetworkRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Labels` | [`Labels2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/net-standard-library/models/structures/labels-2.md) | Optional | User-defined labels (key-value pairs) |
| `Name` | `string` | Optional | New network name |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

UpdateNetworkRequest updateNetworkRequest = new UpdateNetworkRequest
{
    Labels = new Labels2
    {
        Labelkey = "labelkey4",
    },
    Name = "new-name",
};
```



