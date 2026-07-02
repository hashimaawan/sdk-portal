# V2 Databases Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `databases` | [`?(Database1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/database-1.md) | Optional | - | getDatabases(): ?array | setDatabases(?array databases): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesResponseBuilder;
use DigitalOceanApiLib\Models\Builders\Database1Builder;
use DigitalOceanApiLib\Models\Engine1;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\MaintenanceWindowBuilder;

$v2DatabasesResponse = V2DatabasesResponseBuilder::init()
    ->databases(
        [
            Database1Builder::init(
                Engine1::REDIS,
                'name6',
                242,
                'region2',
                'size4'
            )
                ->connection(
                    ConnectionBuilder::init()
                        ->database('database2')
                        ->host('host0')
                        ->password('password2')
                        ->port(174)
                        ->ssl(false)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->dbNames(
                    [
                        'db_names7',
                        'db_names8'
                    ]
                )
                ->id('0000031c-0000-0000-0000-000000000000')
                ->maintenanceWindow(
                    MaintenanceWindowBuilder::init(
                        'day0',
                        'hour8'
                    )
                        ->description(
                            [
                                'description3',
                                'description2'
                            ]
                        )
                        ->pending(false)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



