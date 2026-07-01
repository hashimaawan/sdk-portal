# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/net-standard-library/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type object.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `Distance` | `long?` | Optional | route distance in meters |
| `Duration` | `long?` | Optional | route duration in seconds |
| `Mode` | [`Mode?`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/net-standard-library/models/enumerations/mode.md) | Optional | travel mode |
| `Polyline` | `string` | Optional | route path compatible with Google polyline encoding algorithm |
| `AdditionalProperties` | `object this[string key]` | Optional | - |


# Example

```csharp
using FurkotTrips.Standard.Models;
using FurkotTrips.Standard.Utilities;

Route route = new Route
{
    Distance = 134L,
    Duration = 168L,
    Mode = Mode.Car,
    Polyline = "polyline0",
    ["exampleAdditionalProperty"] = ApiHelper.JsonDeserialize<object>("{\"key1\":\"val1\",\"key2\":\"val2\"}"),
};
```



