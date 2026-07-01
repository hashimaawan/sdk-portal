# Coordinates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkNvb3JkaW5hdGVz

geographical coordinates of the stop

*This model accepts additional fields of type array.*


# Class Name

`Coordinates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `lat` | `?float` | Optional | latitude | getLat(): ?float | setLat(?float lat): void |
| `lon` | `?float` | Optional | longitude | getLon(): ?float | setLon(?float lon): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use FurkotTripsLib\Models\Builders\CoordinatesBuilder;
use FurkotTripsLib\ApiHelper;

$coordinates = CoordinatesBuilder::init()
    ->lat(182.98)
    ->lon(16.08)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



