# Locations Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/java/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2U


# Class Name

`LocationsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Locations` | [`List<Location>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/java/models/structures/location.md) | Required | - | List<Location> getLocations() | setLocations(List<Location> locations) |


# Example

```java
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.LocationsResponse;
import java.util.Arrays;

LocationsResponse locationsResponse = new LocationsResponse.Builder(
    Arrays.asList(
        new Location.Builder(
            "Falkenstein",
            "DE",
            "Falkenstein DC Park 1",
            1D,
            50.47612D,
            12.370071D,
            "fsn1",
            "eu-central"
        )
        .build()
    )
)
.build();
```



