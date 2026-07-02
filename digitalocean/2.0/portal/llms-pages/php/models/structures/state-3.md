# State 3

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXRlMw

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`State3`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `previousOutage` | [`?PreviousOutage`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/previous-outage.md) | Optional | - | getPreviousOutage(): ?PreviousOutage | setPreviousOutage(?PreviousOutage previousOutage): void |
| `regions` | [`?Regions`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/regions.md) | Optional | A map of region to regional state | getRegions(): ?Regions | setRegions(?Regions regions): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\State3Builder;
use DigitalOceanApiLib\Models\Builders\PreviousOutageBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\RegionsBuilder;
use DigitalOceanApiLib\Models\Builders\EuWestBuilder;
use DigitalOceanApiLib\Models\Status16;

$state3 = State3Builder::init()
    ->previousOutage(
        PreviousOutageBuilder::init()
            ->durationSeconds(16)
            ->endedAt('ended_at4')
            ->region('region8')
            ->startedAt('started_at4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->regions(
        RegionsBuilder::init()
            ->euWest(
                EuWestBuilder::init()
                    ->status(Status16::DOWN)
                    ->statusChangedAt('status_changed_at4')
                    ->thirtyDayUptimePercentage(227.78)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->usEast(
                EuWestBuilder::init()
                    ->status(Status16::DOWN)
                    ->statusChangedAt('status_changed_at4')
                    ->thirtyDayUptimePercentage(121.56)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



