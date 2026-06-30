# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/java/x-redirect/JTI0bSUyRlRyaXA


# Class Name

`Trip`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Begin` | `LocalDateTime` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm | LocalDateTime getBegin() | setBegin(LocalDateTime begin) |
| `Description` | `String` | Optional | description of the trip (truncated to 200 characters) | String getDescription() | setDescription(String description) |
| `End` | `LocalDateTime` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm | LocalDateTime getEnd() | setEnd(LocalDateTime end) |
| `Id` | `String` | Optional | Unique ID of the trip | String getId() | setId(String id) |
| `Name` | `String` | Optional | name of the trip | String getName() | setName(String name) |


# Example

```java
import com.furkot.trips.DateTimeHelper;
import com.furkot.trips.models.Trip;

Trip trip = new Trip.Builder()
    .begin(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .description("description8")
    .end(DateTimeHelper.fromRfc8601DateTime("2016-03-13T12:52:32.123Z"))
    .id("id8")
    .name("name8")
    .build();
```



