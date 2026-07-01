# Locations Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/java/x-redirect/JTI0bSUyRkxvY2F0aW9ucyUyNTIwUmVzcG9uc2Ux


# Class Name

`LocationsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `Location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/java/models/structures/location.md) | Required | - | Location getLocation() | setLocation(Location location) |


# Example

```java
import cloud.hetzner.api.models.Location;
import cloud.hetzner.api.models.LocationsResponse1;

LocationsResponse1 locationsResponse1 = new LocationsResponse1.Builder(
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
.build();
```



