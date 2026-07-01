# Attach Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkF0dGFjaFZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`AttachVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `bool?` | Optional | Auto-mount the Volume after attaching it |
| `Server` | `int` | Required | ID of the Server the Volume will be attached to |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

AttachVolumeRequest attachVolumeRequest = new AttachVolumeRequest
{
    Server = 43,
    Automount = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



