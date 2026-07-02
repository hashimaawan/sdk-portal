# Options 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk9wdGlvbnMx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Options1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `regions` | [`?(Region4[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region-4.md) | Optional | - | getRegions(): ?array | setRegions(?array regions): void |
| `sizes` | [`?(Size1[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/size-1.md) | Optional | - | getSizes(): ?array | setSizes(?array sizes): void |
| `versions` | [`?(AvailableUpgradeVersion[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/available-upgrade-version.md) | Optional | - | getVersions(): ?array | setVersions(?array versions): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Options1Builder;
use DigitalOceanApiLib\Models\Builders\Region4Builder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\Size1Builder;
use DigitalOceanApiLib\Models\Builders\AvailableUpgradeVersionBuilder;

$options1 = Options1Builder::init()
    ->regions(
        [
            Region4Builder::init()
                ->name('name0')
                ->slug('slug6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->sizes(
        [
            Size1Builder::init()
                ->name('name0')
                ->slug('slug6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Size1Builder::init()
                ->name('name0')
                ->slug('slug6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->versions(
        [
            AvailableUpgradeVersionBuilder::init()
                ->kubernetesVersion('kubernetes_version6')
                ->slug('slug4')
                ->supportedFeatures(
                    [
                        'supported_features7',
                        'supported_features8'
                    ]
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



