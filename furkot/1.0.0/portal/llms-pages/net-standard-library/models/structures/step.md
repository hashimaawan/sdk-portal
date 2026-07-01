# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlN0ZXA


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Address` | `string` | Optional | address of the stop |
| `Arrival` | `DateTime?` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm |
| `Coordinates` | [`Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/structures/coordinates.md) | Optional | geographical coordinates of the stop |
| `Departure` | `DateTime?` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm |
| `Name` | `string` | Optional | name of the stop |
| `Nights` | `long?` | Optional | number of nights |
| `Passthru` | `bool?` | Optional | true for pass-through points anchoring route |
| `Route` | [`Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/structures/route.md) | Optional | route leading to the stop |
| `Url` | `string` | Optional | url of the page with more information about the stop |


# Example

```csharp
using FurkotTrips.Standard.Models;
using System.Globalization;

Step step = new Step
{
    Address = "address4",
    Arrival = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Coordinates = new Coordinates
    {
        Lat = 182.98,
        Lon = 16.08,
    },
    Departure = DateTime.ParseExact("2016-03-13T12:52:32.123Z", "yyyy'-'MM'-'dd'T'HH':'mm':'ss.FFFFFFFK",
        provider: CultureInfo.InvariantCulture,
        DateTimeStyles.RoundtripKind),
    Name = "name8",
};
```



