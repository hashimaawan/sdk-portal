# Location 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRkxvY2F0aW9uMTY

Location of the Volume. Volume can only be attached to Servers in the same Location.

*This model accepts additional fields of type object.*


# Class Name

`Location16`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `City` | `string` | Required | City the Location is closest to |
| `Country` | `string` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in |
| `Description` | `string` | Required | Description of the Location |
| `Id` | `double` | Required | ID of the Location |
| `Latitude` | `double` | Required | Latitude of the city closest to the Location |
| `Longitude` | `double` | Required | Longitude of the city closest to the Location |
| `Name` | `string` | Required | Unique identifier of the Location |
| `NetworkZone` | `string` | Required | Name of network zone this Location resides in |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using HetznerCloudApi.Standard.Models;
using HetznerCloudApi.Standard.Utilities;

Location16 location16 = new Location16
{
    City = "Falkenstein",
    Country = "DE",
    Description = "Falkenstein DC Park 1",
    Id = 1,
    Latitude = 50.47612,
    Longitude = 12.370071,
    Name = "fsn1",
    NetworkZone = "eu-central",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



