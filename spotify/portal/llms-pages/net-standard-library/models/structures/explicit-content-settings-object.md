# Explicit Content Settings Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/net-standard-library/x-redirect/JTI0bSUyRkV4cGxpY2l0Q29udGVudFNldHRpbmdzT2JqZWN0

*This model accepts additional fields of type object.*


# Class Name

`ExplicitContentSettingsObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `FilterEnabled` | `bool?` | Optional | When `true`, indicates that explicit content should not be played. |
| `FilterLocked` | `bool?` | Optional | When `true`, indicates that the explicit content setting is locked and can't be changed by the user. |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Models;
using SpotifyWebApiWithFixesAndImprovementsFromSonallux.Standard.Utilities;

ExplicitContentSettingsObject explicitContentSettingsObject = new ExplicitContentSettingsObject
{
    FilterEnabled = false,
    FilterLocked = false,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



