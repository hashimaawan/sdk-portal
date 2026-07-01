# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Image` | `string` | Required | ID or name of Image to rebuilt from. |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

RebuildServerRequest rebuildServerRequest = new RebuildServerRequest
{
    Image = "ubuntu-20.04",
};
```



