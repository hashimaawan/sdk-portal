# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Lat` | `Double` | Optional | latitude | Double getLat() | setLat(Double lat) |
| `Lon` | `Double` | Optional | longitude | Double getLon() | setLon(Double lon) |


# Example

```java
import com.furkot.trips.models.Coordinates;

Coordinates coordinates = new Coordinates.Builder()
    .lat(182.98D)
    .lon(16.08D)
    .build();
```



