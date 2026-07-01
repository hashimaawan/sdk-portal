# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type Object.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Distance` | `Long` | Optional | route distance in meters | Long getDistance() | setDistance(Long distance) |
| `Duration` | `Long` | Optional | route duration in seconds | Long getDuration() | setDuration(Long duration) |
| `Mode` | [`Mode`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/models/enumerations/mode.md) | Optional | travel mode | Mode getMode() | setMode(Mode mode) |
| `Polyline` | `String` | Optional | route path compatible with Google polyline encoding algorithm | String getPolyline() | setPolyline(String polyline) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.furkot.trips.ApiHelper;
import com.furkot.trips.models.Mode;
import com.furkot.trips.models.Route;
import java.io.IOException;

Route route = new Route.Builder()
    .distance(134L)
    .duration(168L)
    .mode(Mode.CAR)
    .polyline("polyline0")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



