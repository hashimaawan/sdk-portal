# Trip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/furkot/#/php/x-redirect/JTI0bSUyRlRyaXA


# Class Name

`Trip`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `begin` | `?DateTime` | Optional | begin of the trip in its local timezone as YYYY-MM-DDThh:mm | getBegin(): ?\DateTime | setBegin(?\DateTime begin): void |
| `description` | `?string` | Optional | description of the trip (truncated to 200 characters) | getDescription(): ?string | setDescription(?string description): void |
| `end` | `?DateTime` | Optional | end of the trip in its local timezone as YYYY-MM-DDThh:mm | getEnd(): ?\DateTime | setEnd(?\DateTime end): void |
| `id` | `?string` | Optional | Unique ID of the trip | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | name of the trip | getName(): ?string | setName(?string name): void |


# Example

```php
use FurkotTripsLib\Models\Builders\TripBuilder;
use FurkotTripsLib\Utils\DateTimeHelper;

$trip = TripBuilder::init()
    ->begin(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->description('description8')
    ->end(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->id('id8')
    ->name('name8')
    ->build();
```



