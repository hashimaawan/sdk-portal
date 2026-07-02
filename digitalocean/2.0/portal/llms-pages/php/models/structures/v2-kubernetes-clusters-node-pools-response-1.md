# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nodePool` | [`?NodePool`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/node-pool.md) | Optional | - | getNodePool(): ?NodePool | setNodePool(?NodePool nodePool): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersNodePoolsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\NodePoolBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\NodeBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Status10Builder;
use DigitalOceanApiLib\Models\State1;

$v2KubernetesClustersNodePoolsResponse1 = V2KubernetesClustersNodePoolsResponse1Builder::init()
    ->nodePool(
        NodePoolBuilder::init(
            's-1vcpu-2gb',
            3,
            'new-pool'
        )
            ->autoScale(true)
            ->id('cdda885e-7663-40c8-bc74-3a036c66545d')
            ->labels(null)
            ->maxNodes(6)
            ->minNodes(3)
            ->nodes(
                [
                    NodeBuilder::init()
                        ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
                        ->dropletId(' ')
                        ->id('478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f')
                        ->name(' ')
                        ->status(
                            Status10Builder::init()
                                ->state(State1::PROVISIONING)
                                ->build()
                        )
                        ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
                        ->build(),
                    NodeBuilder::init()
                        ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
                        ->dropletId(' ')
                        ->id('ad12e744-c2a9-473d-8aa9-be5680500eb1')
                        ->name(' ')
                        ->status(
                            Status10Builder::init()
                                ->state(State1::PROVISIONING)
                                ->build()
                        )
                        ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
                        ->build(),
                    NodeBuilder::init()
                        ->createdAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
                        ->dropletId(' ')
                        ->id('e46e8d07-f58f-4ff1-9737-97246364400e')
                        ->name(' ')
                        ->status(
                            Status10Builder::init()
                                ->state(State1::PROVISIONING)
                                ->build()
                        )
                        ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2018-11-15T16:00:11Z'))
                        ->build()
                ]
            )
            ->tags(
                [
                    'production',
                    'web-team',
                    'front-end',
                    'k8s',
                    'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
                    'k8s:worker'
                ]
            )
            ->taints(
                []
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



