# Images Actions Change Protection Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwQWN0aW9ucyUyNTIwQ2hhbmdlJTI1MjBQcm90ZWN0aW9uJTI1MjBSZXF1ZXN0


# Class Name

`ImagesActionsChangeProtectionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Delete` | `bool?` | Optional | If true, prevents the snapshot from being deleted |


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

ImagesActionsChangeProtectionRequest imagesActionsChangeProtectionRequest = new ImagesActionsChangeProtectionRequest
{
    Delete = true,
};
```



