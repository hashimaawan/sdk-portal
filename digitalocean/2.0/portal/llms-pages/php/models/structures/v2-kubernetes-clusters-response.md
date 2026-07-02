# V2 Kubernetes Clusters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kubernetesClusters` | [`?(KubernetesCluster[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/kubernetes-cluster.md) | Optional | - | getKubernetesClusters(): ?array | setKubernetesClusters(?array kubernetesClusters): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\KubernetesClusterBuilder;
use DigitalOceanApiLib\Models\Builders\NodePoolBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2KubernetesClustersResponse = V2KubernetesClustersResponseBuilder::init(
    MetaBuilder::init(
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->kubernetesClusters(
        [
            KubernetesClusterBuilder::init(
                'name2',
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
                        ->build(),
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
                        ->build(),
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
                ],
                'region8',
                'version8'
            )
                ->autoUpgrade(false)
                ->clusterSubnet('cluster_subnet4')
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->endpoint('endpoint0')
                ->ha(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            KubernetesClusterBuilder::init(
                'name2',
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
                        ->build(),
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
                        ->build(),
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
                ],
                'region8',
                'version8'
            )
                ->autoUpgrade(false)
                ->clusterSubnet('cluster_subnet4')
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->endpoint('endpoint0')
                ->ha(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            KubernetesClusterBuilder::init(
                'name2',
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
                        ->build(),
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
                        ->build(),
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
                ],
                'region8',
                'version8'
            )
                ->autoUpgrade(false)
                ->clusterSubnet('cluster_subnet4')
                ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->endpoint('endpoint0')
                ->ha(false)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('last6')
                    ->next('next2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



