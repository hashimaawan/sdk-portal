# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/php/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `lat` | `?float` | Optional | latitude | getLat(): ?float | setLat(?float lat): void |
| `lon` | `?float` | Optional | longitude | getLon(): ?float | setLon(?float lon): void |


# Example

```php
use FurkotTripsLib\Models\Builders\CoordinatesBuilder;

$coordinates = CoordinatesBuilder::init()
    ->lat(182.98)
    ->lon(16.08)
    ->build();
```



