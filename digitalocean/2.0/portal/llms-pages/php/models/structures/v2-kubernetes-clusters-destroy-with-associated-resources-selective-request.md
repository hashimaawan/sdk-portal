# V2 Kubernetes Clusters Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing the IDs of resources to be destroyed along with their associated with a Kubernetes cluster.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `loadBalancers` | `?(string[])` | Optional | A list of IDs for associated load balancers to destroy along with the cluster. | getLoadBalancers(): ?array | setLoadBalancers(?array loadBalancers): void |
| `volumeSnapshots` | `?(string[])` | Optional | A list of IDs for associated volume snapshots to destroy along with the cluster. | getVolumeSnapshots(): ?array | setVolumeSnapshots(?array volumeSnapshots): void |
| `volumes` | `?(string[])` | Optional | A list of IDs for associated volumes to destroy along with the cluster. | getVolumes(): ?array | setVolumes(?array volumes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest = V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequestBuilder::init()
    ->loadBalancers(
        [
            '4de7ac8b-495b-4884-9a69-1050c6793cd6'
        ]
    )
    ->volumeSnapshots(
        [
            'edb0478d-7436-11ea-86e6-0a58ac144b91'
        ]
    )
    ->volumes(
        [
            'ba49449a-7435-11ea-b89e-0a58ac14480f'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



