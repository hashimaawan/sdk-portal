# V2 Registry Options Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZWdpc3RyeSUyNTIwT3B0aW9ucyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2RegistryOptionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `options` | [`?Options2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/options-2.md) | Optional | - | getOptions(): ?Options2 | setOptions(?Options2 options): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2RegistryOptionsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\Options2Builder;
use DigitalOceanApiLib\Models\Builders\SubscriptionTierBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2RegistryOptionsResponse = V2RegistryOptionsResponseBuilder::init()
    ->options(
        Options2Builder::init()
            ->availableRegions(
                [
                    'available_regions9'
                ]
            )
            ->subscriptionTiers(
                [
                    SubscriptionTierBuilder::init()
                        ->allowStorageOverage(false)
                        ->includedBandwidthBytes(172)
                        ->includedRepositories(194)
                        ->includedStorageBytes(242)
                        ->monthlyPriceInCents(236)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    SubscriptionTierBuilder::init()
                        ->allowStorageOverage(false)
                        ->includedBandwidthBytes(172)
                        ->includedRepositories(194)
                        ->includedStorageBytes(242)
                        ->monthlyPriceInCents(236)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build(),
                    SubscriptionTierBuilder::init()
                        ->allowStorageOverage(false)
                        ->includedBandwidthBytes(172)
                        ->includedRepositories(194)
                        ->includedStorageBytes(242)
                        ->monthlyPriceInCents(236)
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



