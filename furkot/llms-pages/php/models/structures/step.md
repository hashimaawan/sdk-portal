# Step

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/php/x-redirect/JTI0bSUyRlN0ZXA


# Class Name

`Step`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `address` | `?string` | Optional | address of the stop | getAddress(): ?string | setAddress(?string address): void |
| `arrival` | `?DateTime` | Optional | arrival at the stop in its local timezone as YYYY-MM-DDThh:mm | getArrival(): ?\DateTime | setArrival(?\DateTime arrival): void |
| `coordinates` | [`?Coordinates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/php/models/structures/coordinates.md) | Optional | geographical coordinates of the stop | getCoordinates(): ?Coordinates | setCoordinates(?Coordinates coordinates): void |
| `departure` | `?DateTime` | Optional | departure from the stop in its local timezone as YYYY-MM-DDThh:mm | getDeparture(): ?\DateTime | setDeparture(?\DateTime departure): void |
| `name` | `?string` | Optional | name of the stop | getName(): ?string | setName(?string name): void |
| `nights` | `?int` | Optional | number of nights | getNights(): ?int | setNights(?int nights): void |
| `passthru` | `?bool` | Optional | true for pass-through points anchoring route | getPassthru(): ?bool | setPassthru(?bool passthru): void |
| `route` | [`?Route`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/llms-pages/php/models/structures/route.md) | Optional | route leading to the stop | getRoute(): ?Route | setRoute(?Route route): void |
| `url` | `?string` | Optional | url of the page with more information about the stop | getUrl(): ?string | setUrl(?string url): void |


# Example

```php
use FurkotTripsLib\Models\Builders\StepBuilder;
use FurkotTripsLib\Utils\DateTimeHelper;
use FurkotTripsLib\Models\Builders\CoordinatesBuilder;

$step = StepBuilder::init()
    ->address('address4')
    ->arrival(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->coordinates(
        CoordinatesBuilder::init()
            ->lat(182.98)
            ->lon(16.08)
            ->build()
    )
    ->departure(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->name('name8')
    ->build();
```



