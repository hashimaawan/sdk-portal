# V2 Droplets Actions Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVzcG9uc2Uy

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsActionsResponse2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsActionsResponse2Builder;
use DigitalOceanApiLib\Models\Builders\ActionBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2DropletsActionsResponse2 = V2DropletsActionsResponse2Builder::init()
    ->action(
        ActionBuilder::init()
            ->completedAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->id(238)
            ->region(
                RegionBuilder::init(
                    false,
                    [
                        'features7',
                        'features8',
                        'features9'
                    ],
                    'name6',
                    [
                        'sizes6'
                    ],
                    'slug0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->regionSlug('region_slug0')
            ->resourceId(66)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



