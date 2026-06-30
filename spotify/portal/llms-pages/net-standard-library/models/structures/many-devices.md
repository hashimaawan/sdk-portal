# Many Devices

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRk1hbnlEZXZpY2Vz

*This model accepts additional fields of type object.*


# Class Name

`ManyDevices`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Devices` | [`List<DeviceObject>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/net-standard-library/models/structures/device-object.md) | Required | - |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;
using System.Collections.Generic;

ManyDevices manyDevices = new ManyDevices
{
    Devices = new List<DeviceObject>
    {
        new DeviceObject
        {
            Id = "id4",
            IsActive = false,
            IsPrivateSession = false,
            IsRestricted = false,
            Name = "Kitchen speaker",
            Type = "computer",
            VolumePercent = 59,
            ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
        },
    },
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



