# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type Object.*


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Lat` | `Double` | Optional | latitude | Double getLat() | setLat(Double lat) |
| `Lon` | `Double` | Optional | longitude | Double getLon() | setLon(Double lon) |
| `AdditionalProperties` | `Map<String, Object>` | Optional | - | Object getAdditionalProperty(String key) | additionalProperty(String key, Object value) |


# Example

```java
import com.furkot.trips.ApiHelper;
import com.furkot.trips.models.Coordinates;
import java.io.IOException;

Coordinates coordinates = new Coordinates.Builder()
    .lat(182.98D)
    .lon(16.08D)
.additionalProperty("exampleAdditionalProperty", ApiHelper.deserialize("{\"key1\":\"val1\",\"key2\":\"val2\"}"))
    .build();
```



