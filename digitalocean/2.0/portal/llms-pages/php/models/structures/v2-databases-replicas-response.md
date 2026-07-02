# V2 Databases Replicas Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEYXRhYmFzZXMlMjUyMFJlcGxpY2FzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DatabasesReplicasResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `replicas` | [`?(Replica[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/replica.md) | Optional | - | getReplicas(): ?array | setReplicas(?array replicas): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DatabasesReplicasResponseBuilder;
use DigitalOceanApiLib\Models\Builders\ReplicaBuilder;
use DigitalOceanApiLib\Models\Builders\ConnectionBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\PrivateConnectionBuilder;

$v2DatabasesReplicasResponse = V2DatabasesReplicasResponseBuilder::init()
    ->replicas(
        [
            ReplicaBuilder::init(
                'name6'
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
                ->id('000022b6-0000-0000-0000-000000000000')
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
                ->privateNetworkUuid('private_network_uuid6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ReplicaBuilder::init(
                'name6'
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
                ->id('000022b6-0000-0000-0000-000000000000')
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
                ->privateNetworkUuid('private_network_uuid6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



