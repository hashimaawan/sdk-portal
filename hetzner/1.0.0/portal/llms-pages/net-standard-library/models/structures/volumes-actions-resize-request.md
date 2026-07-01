# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Size` | `double` | Required | New Volume size in GB (must be greater than current size) |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

VolumesActionsResizeRequest volumesActionsResizeRequest = new VolumesActionsResizeRequest
{
    Size = 50,
};
```



