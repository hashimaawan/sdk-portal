# Regions

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlZ2lvbnM

A map of region to regional state

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Regions`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `euWest` | [`?EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/eu-west.md) | Optional | - | getEuWest(): ?EuWest | setEuWest(?EuWest euWest): void |
| `usEast` | [`?EuWest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/eu-west.md) | Optional | - | getUsEast(): ?EuWest | setUsEast(?EuWest usEast): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\RegionsBuilder;
use DigitalOceanApiLib\Models\Builders\EuWestBuilder;
use DigitalOceanApiLib\Models\Status16;
use DigitalOceanApiLib\ApiHelper;

$regions = RegionsBuilder::init()
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
    ->build();
```



