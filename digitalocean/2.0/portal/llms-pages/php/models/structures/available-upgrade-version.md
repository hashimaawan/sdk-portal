# Available Upgrade Version

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkF2YWlsYWJsZVVwZ3JhZGVWZXJzaW9u

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`AvailableUpgradeVersion`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `kubernetesVersion` | `?string` | Optional | The upstream version string for the version of Kubernetes provided by a given slug. | getKubernetesVersion(): ?string | setKubernetesVersion(?string kubernetesVersion): void |
| `slug` | `?string` | Optional | The slug identifier for an available version of Kubernetes for use when creating or updating a cluster. The string contains both the upstream version of Kubernetes as well as the DigitalOcean revision. | getSlug(): ?string | setSlug(?string slug): void |
| `supportedFeatures` | `?(string[])` | Optional | The features available with the version of Kubernetes provided by a given slug. | getSupportedFeatures(): ?array | setSupportedFeatures(?array supportedFeatures): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\AvailableUpgradeVersionBuilder;
use DigitalOceanApiLib\ApiHelper;

$availableUpgradeVersion = AvailableUpgradeVersionBuilder::init()
    ->kubernetesVersion('1.16.13')
    ->slug('1.16.13-do.0')
    ->supportedFeatures(
        [
            'cluster-autoscaler',
            'docr-integration',
            'token-authentication'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



