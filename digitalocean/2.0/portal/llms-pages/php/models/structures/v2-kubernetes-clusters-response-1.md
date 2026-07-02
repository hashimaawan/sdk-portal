# V2 Kubernetes Clusters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kubernetesCluster` | [`?KubernetesCluster`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/kubernetes-cluster.md) | Optional | - | getKubernetesCluster(): ?KubernetesCluster | setKubernetesCluster(?KubernetesCluster kubernetesCluster): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersResponse1Builder;
use DigitalOceanApiLib\Models\Builders\KubernetesClusterBuilder;
use DigitalOceanApiLib\Models\Builders\NodePoolBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Utils\DateTimeHelper;

$v2KubernetesClustersResponse1 = V2KubernetesClustersResponse1Builder::init()
    ->kubernetesCluster(
        KubernetesClusterBuilder::init(
            'name8',
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
                    ->build()
            ],
            'region4',
            'version4'
        )
            ->autoUpgrade(false)
            ->clusterSubnet('cluster_subnet0')
            ->createdAt(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->endpoint('endpoint6')
            ->ha(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



