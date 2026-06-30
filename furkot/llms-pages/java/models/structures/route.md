# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/java/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Distance` | `Long` | Optional | route distance in meters | Long getDistance() | setDistance(Long distance) |
| `Duration` | `Long` | Optional | route duration in seconds | Long getDuration() | setDuration(Long duration) |
| `Mode` | [`ModeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/models/enumerations/mode.md) | Optional | travel mode | ModeEnum getMode() | setMode(ModeEnum mode) |
| `Polyline` | `String` | Optional | route path compatible with Google polyline encoding algorithm | String getPolyline() | setPolyline(String polyline) |


# Example

```java
import com.furkot.trips.models.ModeEnum;
import com.furkot.trips.models.Route;

Route route = new Route.Builder()
    .distance(134L)
    .duration(168L)
    .mode(ModeEnum.CAR)
    .polyline("polyline0")
    .build();
```



