# V2 Kubernetes Clusters User Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXNlciUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUserResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kubernetesClusterUser` | [`?KubernetesClusterUser`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/kubernetes-cluster-user.md) | Optional | - | getKubernetesClusterUser(): ?KubernetesClusterUser | setKubernetesClusterUser(?KubernetesClusterUser kubernetesClusterUser): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersUserResponseBuilder;
use DigitalOceanApiLib\Models\Builders\KubernetesClusterUserBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersUserResponse = V2KubernetesClustersUserResponseBuilder::init()
    ->kubernetesClusterUser(
        KubernetesClusterUserBuilder::init()
            ->groups(
                [
                    'groups8'
                ]
            )
            ->username('username6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



