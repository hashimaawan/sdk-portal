# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/java/x-redirect/JTI0bSUyRlN0ZXA

*This model accepts additional fields of type Object.*


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Optional | address of the stop | String getAddress() | setAddress(String address) |
| `Arrival` | `LocalDateTime` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm | LocalDateTime getArrival() | setArrival(LocalDateTime arrival) |
| `Coordinates` | [`Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/models/structures/coordinates.md) | Optional | geographical coordinates of the stop | Coordinates getCoordinates() | setCoordinates(Coordinates coordinates) |
| `Departure` | `LocalDateTime` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm | LocalDateTime getDeparture() | setDeparture(LocalDateTime departure) |
| `Name` | `String` | Optional | name of the stop | String getName() | setName(String name) |
| `Nights` | `Long` | Optional | number of nights | Long getNights() | setNights(Long nights) |
| `Passthru` | `Boolean` | Optional | true for pass-through points anchoring route | Boolean getPassthru() | setPassthru(Boolean passthru) |
| `Route` | [`Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/java/models/structures/route.md) | Optional | route leading to the stop | Route getRoute() | setRoute(Route route) |
| `Url` | `String` | Optional | url of the page with more information about the stop | String getUrl() | setUrl(String url) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.furkot.trips.ApiHelper;
import com.furkot.trips.DateTimeHelper;
import com.furkot.trips.models.Coordinates;
import com.furkot.trips.models.Step;
import java.io.IOException;

Step step = new Step.Builder()
    .address("address4")
    .arrival(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .coordinates(new Coordinates.Builder()
        .lat(182.98D)
        .lon(16.08D)
    .additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
        .build())
    .departure(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .name("name8")
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



