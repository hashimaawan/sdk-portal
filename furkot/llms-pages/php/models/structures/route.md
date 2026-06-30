# Route

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/php/x-redirect/JTI0bSUyRlJvdXRl

route leading to the stop


# Class Name

`Route`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `distance` | `?int` | Optional | route distance in meters | getDistance(): ?int | setDistance(?int distance): void |
| `duration` | `?int` | Optional | route duration in seconds | getDuration(): ?int | setDuration(?int duration): void |
| `mode` | [`?string(ModeEnum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/php/models/enumerations/mode.md) | Optional | travel mode | getMode(): ?string | setMode(?string mode): void |
| `polyline` | `?string` | Optional | route path compatible with Google polyline encoding algorithm | getPolyline(): ?string | setPolyline(?string polyline): void |


# Example

```php
use FurkotTripsLib\Models\Builders\RouteBuilder;
use FurkotTripsLib\Models\ModeEnum;

$route = RouteBuilder::init()
    ->distance(134)
    ->duration(168)
    ->mode(ModeEnum::CAR)
    ->polyline('polyline0')
    ->build();
```



