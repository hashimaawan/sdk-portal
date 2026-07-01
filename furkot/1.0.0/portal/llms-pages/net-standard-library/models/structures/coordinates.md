# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type object.*


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Lat` | `double?` | Optional | latitude |
| `Lon` | `double?` | Optional | longitude |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using FurkotTrips.Standard.Models;
using FurkotTrips.Standard.Utilities;

Coordinates coordinates = new Coordinates
{
    Lat = 182.98,
    Lon = 16.08,
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



