# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop

*This model accepts additional fields of type array.*


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `distance` | `?int` | Optional | route distance in meters | getDistance(): ?int | setDistance(?int distance): void |
| `duration` | `?int` | Optional | route duration in seconds | getDuration(): ?int | setDuration(?int duration): void |
| `mode` | [`?string(Mode)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/1.0.0/portal/llms-pages/php/models/enumerations/mode.md) | Optional | travel mode | getMode(): ?string | setMode(?string mode): void |
| `polyline` | `?string` | Optional | route path compatible with Google polyline encoding algorithm | getPolyline(): ?string | setPolyline(?string polyline): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use FurkotTripsLib\Models\Builders\RouteBuilder;
use FurkotTripsLib\Models\Mode;
use FurkotTripsLib\ApiHelper;

$route = RouteBuilder::init()
    ->distance(134)
    ->duration(168)
    ->mode(Mode::CAR)
    ->polyline('polyline0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



