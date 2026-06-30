# Device Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/net-standard-library/x-redirect/JTI0bSUyRkRldmljZU9iamVjdA

*This model accepts additional fields of type object.*


# Class Name

`DeviceObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Id` | `string` | Optional | The device ID. This ID is unique and persistent to some extent. However, this is not guaranteed and any cached `device_id` should periodically be cleared out and refetched as necessary. |
| `IsActive` | `bool?` | Optional | If this device is the currently active device. |
| `IsPrivateSession` | `bool?` | Optional | If this device is currently in a private session. |
| `IsRestricted` | `bool?` | Optional | Whether controlling this device is restricted. At present if this is "true" then no Web API commands will be accepted by this device. |
| `Name` | `string` | Optional | A human-readable name for the device. Some devices have a name that the user can configure (e.g. \"Loudest speaker\") and some devices have a generic name associated with the manufacturer or device model. |
| `Type` | `string` | Optional | Device type, such as "computer", "smartphone" or "speaker". |
| `VolumePercent` | `int?` | Optional | The current volume in percent.<br><br>**Constraints**: `>= 0`, `<= 100` |
| `SupportsVolume` | `bool?` | Optional | If this device can be used to set the volume. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

DeviceObject deviceObject = new DeviceObject
{
    Id = "id0",
    IsActive = false,
    IsPrivateSession = false,
    IsRestricted = false,
    Name = "Kitchen speaker",
    Type = "computer",
    VolumePercent = 59,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



