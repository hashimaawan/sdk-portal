# Kubernetes Cluster User

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVyVXNlcg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`KubernetesClusterUser`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `groups` | `?(string[])` | Optional | A list of in-cluster groups that the user belongs to. | getGroups(): ?array | setGroups(?array groups): void |
| `username` | `?string` | Optional | The username for the cluster admin user. | getUsername(): ?string | setUsername(?string username): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\KubernetesClusterUserBuilder;
use DigitalOceanApiLib\ApiHelper;

$kubernetesClusterUser = KubernetesClusterUserBuilder::init()
    ->groups(
        [
            'k8saas:authenticated'
        ]
    )
    ->username('sammy@digitalocean.com')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



