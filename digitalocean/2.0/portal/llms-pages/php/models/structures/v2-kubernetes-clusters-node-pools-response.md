# V2 Kubernetes Clusters Node Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersNodePoolsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nodePools` | [`?(NodePool[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/node-pool.md) | Optional | - | getNodePools(): ?array | setNodePools(?array nodePools): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersNodePoolsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\NodePoolBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersNodePoolsResponse = V2KubernetesClustersNodePoolsResponseBuilder::init()
    ->nodePools(
        [
            NodePoolBuilder::init(
                'size6',
                206,
                'name4'
            )
                ->autoScale(false)
                ->id('000013be-0000-0000-0000-000000000000')
                ->labels(ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->maxNodes(118)
                ->minNodes(54)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



