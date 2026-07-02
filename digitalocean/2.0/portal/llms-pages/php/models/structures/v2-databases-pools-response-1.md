# V2 Databases Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFBvb2xzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesPoolsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pool` | [`Pool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/pool.md) | Required | - | getPool(): Pool | setPool(Pool pool): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesPoolsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\PoolBuilder;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\PrivateConnectionBuilder;

$v2DatabasesPoolsResponse1 = V2DatabasesPoolsResponse1Builder::init(
    PoolBuilder::init(
        'defaultdb',
        'transaction',
        'backend-pool',
        10
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
        ->privateConnection(
            PrivateConnectionBuilder::init()
                ->database('database4')
                ->host('host4')
                ->password('password8')
                ->port(228)
                ->ssl(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        )
        ->user('doadmin')
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



