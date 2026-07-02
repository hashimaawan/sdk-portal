# V2 Databases Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `database` | [`Database1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/database-1.md) | Required | - | getDatabase(): Database1 | setDatabase(Database1 database): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesResponse1Builder;
use DigitalOceanApiLib\Models\Builders\Database1Builder;
use DigitalOceanApiLib\Models\Engine1;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\MaintenanceWindowBuilder;
use DigitalOceanApiLib\Models\Status4;

$v2DatabasesResponse1 = V2DatabasesResponse1Builder::init(
    Database1Builder::init(
        Engine1::PG,
        'backend',
        2,
        'nyc3',
        'db-s-2vcpu-4gb'
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
        ->createdAt(DateTimeHelper::fromRfc3339DateTime('2019-01-11T18:37:36Z'))
        ->dbNames(
            [
                'doadmin'
            ]
        )
        ->id('9cc10173-e9ea-4176-9dbc-a4cee4c4ff30')
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
        ->privateNetworkUuid('d455e75d-4858-4eec-8c95-da2f0a5f93a7')
        ->projectId('9cc10173-e9ea-4176-9dbc-a4cee4c4ff30')
        ->status(Status4::CREATING)
        ->tags(
            [
                'production'
            ]
        )
        ->version('10')
        ->versionEndOfAvailability('2023-05-09T00:00:00Z')
        ->versionEndOfLife('2023-11-09T00:00:00Z')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



