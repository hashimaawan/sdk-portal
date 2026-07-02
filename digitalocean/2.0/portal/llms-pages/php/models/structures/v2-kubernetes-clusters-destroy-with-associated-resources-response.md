# V2 Kubernetes Clusters Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

An object containing the IDs of resources associated with a Kubernetes cluster.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancers` | [`?(LoadBalancer[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated load balancers that can be destroyed along with the cluster. | getLoadBalancers(): ?array | setLoadBalancers(?array loadBalancers): void |
| `volumeSnapshots` | [`?(LoadBalancer[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volume snapshots that can be destroyed along with the cluster. | getVolumeSnapshots(): ?array | setVolumeSnapshots(?array volumeSnapshots): void |
| `volumes` | [`?(LoadBalancer[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volumes that can be destroyed along with the cluster. | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersDestroyWithAssociatedResourcesResponseBuilder;
use DigitalOceanApiLib\Models\Builders\LoadBalancerBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersDestroyWithAssociatedResourcesResponse = V2KubernetesClustersDestroyWithAssociatedResourcesResponseBuilder::init()
    ->loadBalancers(
        [
            LoadBalancerBuilder::init()
                ->id('4de7ac8b-495b-4884-9a69-1050c6793cd6')
                ->name('lb-001')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->volumeSnapshots(
        [
            LoadBalancerBuilder::init()
                ->id('edb0478d-7436-11ea-86e6-0a58ac144b91')
                ->name('snapshot-001')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->volumes(
        [
            LoadBalancerBuilder::init()
                ->id('ba49449a-7435-11ea-b89e-0a58ac14480f')
                ->name('volume-001')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



