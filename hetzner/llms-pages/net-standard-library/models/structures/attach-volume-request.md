# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `bool?` | Optional | Auto-mount the Volume after attaching it |
| `Server` | `int` | Required | ID of the Server the Volume will be attached to |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

AttachVolumeRequest attachVolumeRequest = new AttachVolumeRequest
{
    Server = 43,
    Automount = false,
};
```



