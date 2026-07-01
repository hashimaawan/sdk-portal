# Create Volume Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNyZWF0ZVZvbHVtZVJlcXVlc3Q

*This model accepts additional fields of type object.*


# Class Name

`CreateVolumeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Automount` | `bool?` | Optional | Auto-mount Volume after attach. `server` must be provided. |
| `Format` | `string` | Optional | Format Volume after creation. One of: `xfs`, `ext4` |
| `Labels` | `object` | Optional | User-defined labels (key-value pairs) |
| `Location` | `string` | Optional | Location to create the Volume in (can be omitted if Server is specified) |
| `Name` | `string` | Required | Name of the volume |
| `Server` | `int?` | Optional | Server to which to attach the Volume once it's created (Volume will be created in the same Location as the server) |
| `Size` | `int` | Required | Size of the Volume in GB |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

CreateVolumeRequest createVolumeRequest = new CreateVolumeRequest
{
    Name = "databases-storage",
    Size = 42,
    Automount = false,
    Format = "xfs",
    Labels = ApiHelper.JsonDeserialize<object>("{\"labelkey\":\"value\"}"),
    Location = "nbg1",
    Server = 182,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



