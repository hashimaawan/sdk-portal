# Location 16

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvY2F0aW9uMTY

Location of the Volume. Volume can only be attached to Servers in the same Location.


# Class Name

`Location16`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `City` | `String` | Required | City the Location is closest to | String getCity() | setCity(String city) |
| `Country` | `String` | Required | ISO 3166-1 alpha-2 code of the country the Location resides in | String getCountry() | setCountry(String country) |
| `Description` | `String` | Required | Description of the Location | String getDescription() | setDescription(String description) |
| `Id` | `double` | Required | ID of the Location | double getId() | setId(double id) |
| `Latitude` | `double` | Required | Latitude of the city closest to the Location | double getLatitude() | setLatitude(double latitude) |
| `Longitude` | `double` | Required | Longitude of the city closest to the Location | double getLongitude() | setLongitude(double longitude) |
| `Name` | `String` | Required | Unique identifier of the Location | String getName() | setName(String name) |
| `NetworkZone` | `String` | Required | Name of network zone this Location resides in | String getNetworkZone() | setNetworkZone(String networkZone) |


# Example

```java
import cloud.hetzner.api.models.Location16;

Location16 location16 = new Location16.Builder(
    "Falkenstein",
    "DE",
    "Falkenstein DC Park 1",
    1D,
    50.47612D,
    12.370071D,
    "fsn1",
    "eu-central"
)
.build();
```



