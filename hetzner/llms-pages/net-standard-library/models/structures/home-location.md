# Home Location

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/net-standard-library/x-redirect/JTI0bSUyRkhvbWVMb2NhdGlvbg

Location the Floating IP was created in. Routing is optimized for this Location.


# Class Name

`HomeLocation`


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


# Example

```csharp
using HetznerCloudAPI.Standard.Models;

HomeLocation homeLocation = new HomeLocation
{
    City = "Falkenstein",
    Country = "DE",
    Description = "Falkenstein DC Park 1",
    Id = 1,
    Latitude = 50.47612,
    Longitude = 12.370071,
    Name = "fsn1",
    NetworkZone = "eu-central",
};
```



