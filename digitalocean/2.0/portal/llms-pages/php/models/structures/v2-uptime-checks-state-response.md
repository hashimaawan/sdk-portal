# V2 Uptime Checks State Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBVcHRpbWUlMjUyMENoZWNrcyUyNTIwU3RhdGUlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2UptimeChecksStateResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `state` | [`?State3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/state-3.md) | Optional | - | getState(): ?State3 | setState(?State3 state): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2UptimeChecksStateResponseBuilder;
use DigitalOceanApiLib\Models\Builders\State3Builder;
use DigitalOceanApiLib\Models\Builders\PreviousOutageBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\RegionsBuilder;
use DigitalOceanApiLib\Models\Builders\EuWestBuilder;
use DigitalOceanApiLib\Models\Status16;

$v2UptimeChecksStateResponse = V2UptimeChecksStateResponseBuilder::init()
    ->state(
        State3Builder::init()
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
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



