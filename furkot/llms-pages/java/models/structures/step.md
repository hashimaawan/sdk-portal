# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/java/x-redirect/JTI0bSUyRlN0ZXA


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Address` | `String` | Optional | address of the stop | String getAddress() | setAddress(String address) |
| `Arrival` | `LocalDateTime` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm | LocalDateTime getArrival() | setArrival(LocalDateTime arrival) |
| `Coordinates` | [`Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/models/structures/coordinates.md) | Optional | geographical coordinates of the stop | Coordinates getCoordinates() | setCoordinates(Coordinates coordinates) |
| `Departure` | `LocalDateTime` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm | LocalDateTime getDeparture() | setDeparture(LocalDateTime departure) |
| `Name` | `String` | Optional | name of the stop | String getName() | setName(String name) |
| `Nights` | `Long` | Optional | number of nights | Long getNights() | setNights(Long nights) |
| `Passthru` | `Boolean` | Optional | true for pass-through points anchoring route | Boolean getPassthru() | setPassthru(Boolean passthru) |
| `Route` | [`Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/java/models/structures/route.md) | Optional | route leading to the stop | Route getRoute() | setRoute(Route route) |
| `Url` | `String` | Optional | url of the page with more information about the stop | String getUrl() | setUrl(String url) |


# Example

```java
import com.furkot.trips.DateTimeHelper;
import com.furkot.trips.models.Coordinates;
import com.furkot.trips.models.Step;

Step step = new Step.Builder()
    .address("address4")
    .arrival(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .coordinates(new Coordinates.Builder()
        .lat(182.98D)
        .lon(16.08D)
        .build())
    .departure(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .name("name8")
    .build();
```



