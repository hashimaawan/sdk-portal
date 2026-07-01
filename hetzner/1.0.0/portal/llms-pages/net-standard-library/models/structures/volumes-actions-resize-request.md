# Volumes Actions Resize Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlZvbHVtZXMlMjUyMEFjdGlvbnMlMjUyMFJlc2l6ZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type object.*


# Class Name

`VolumesActionsResizeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Size` | `double` | Required | New Volume size in GB (must be greater than current size) |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

VolumesActionsResizeRequest volumesActionsResizeRequest = new VolumesActionsResizeRequest
{
    Size = 50,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



