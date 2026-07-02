# V2 Kubernetes Clusters Upgrades Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesClustersUpgradesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `availableUpgradeVersions` | [`?(AvailableUpgradeVersion[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/available-upgrade-version.md) | Optional | - | getAvailableUpgradeVersions(): ?array | setAvailableUpgradeVersions(?array availableUpgradeVersions): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesClustersUpgradesResponseBuilder;
use DigitalOceanApiLib\Models\Builders\AvailableUpgradeVersionBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2KubernetesClustersUpgradesResponse = V2KubernetesClustersUpgradesResponseBuilder::init()
    ->availableUpgradeVersions(
        [
            AvailableUpgradeVersionBuilder::init()
                ->kubernetesVersion('kubernetes_version0')
                ->slug('slug2')
                ->supportedFeatures(
                    [
                        'supported_features3'
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



