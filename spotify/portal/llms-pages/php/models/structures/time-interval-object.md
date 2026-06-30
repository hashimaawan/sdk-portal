# Time Interval Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/php/x-redirect/JTI0bSUyRlRpbWVJbnRlcnZhbE9iamVjdA

*This model accepts additional fields of type array.*


# Class Name

`TimeIntervalObject`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `start` | `?float` | Optional | The starting point (in seconds) of the time interval. | getStart(): ?float | setStart(?float start): void |
| `duration` | `?float` | Optional | The duration (in seconds) of the time interval. | getDuration(): ?float | setDuration(?float duration): void |
| `confidence` | `?float` | Optional | The confidence, from 0.0 to 1.0, of the reliability of the interval.<br><br>**Constraints**: `>= 0`, `<= 1` | getConfidence(): ?float | setConfidence(?float confidence): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\Models\Builders\TimeIntervalObjectBuilder;
use SpotifyWebApiWithFixesAndImprovementsFromSonalluxLib\ApiHelper;

$timeIntervalObject = TimeIntervalObjectBuilder::init()
    ->start(0.49567)
    ->duration(2.18749)
    ->confidence(0.925)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



