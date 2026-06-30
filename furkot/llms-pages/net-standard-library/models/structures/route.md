# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/net-standard-library/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Distance` | `long?` | Optional | route distance in meters |
| `Duration` | `long?` | Optional | route duration in seconds |
| `Mode` | [`ModeEnum?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/net-standard-library/models/enumerations/mode.md) | Optional | travel mode |
| `Polyline` | `string` | Optional | route path compatible with Google polyline encoding algorithm |


# Example

```csharp
using FurkotTrips.Standard.Models;

Route route = new Route
{
    Distance = 134L,
    Duration = 168L,
    Mode = ModeEnum.Car,
    Polyline = "polyline0",
};
```



