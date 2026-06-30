# Volumes Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwUHJvdGVjdGlvbiUyNTIwUmVxdWVzdA


# Class Name

`VolumesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the Volume from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

VolumesActionsChangeProtectionRequest volumesActionsChangeProtectionRequest = new VolumesActionsChangeProtectionRequest
{
    Delete = true,
};
```



