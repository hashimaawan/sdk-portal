# V2 Kubernetes Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBPcHRpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2KubernetesOptionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `options` | [`?Options1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/options-1.md) | Optional | - | getOptions(): ?Options1 | setOptions(?Options1 options): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2KubernetesOptionsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\Options1Builder;
use DigitalOceanApiLib\Models\Builders\Region4Builder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\Size1Builder;
use DigitalOceanApiLib\Models\Builders\AvailableUpgradeVersionBuilder;

$v2KubernetesOptionsResponse = V2KubernetesOptionsResponseBuilder::init()
    ->options(
        Options1Builder::init()
            ->regions(
                [
                    Region4Builder::init()
                        ->name('name0')
                        ->slug('slug6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
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
                        ->build(),
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
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



