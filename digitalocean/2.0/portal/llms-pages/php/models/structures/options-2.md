# Options 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRk9wdGlvbnMy

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Options2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `availableRegions` | `?(string[])` | Optional | - | getAvailableRegions(): ?array | setAvailableRegions(?array availableRegions): void |
| `subscriptionTiers` | [`?(SubscriptionTier[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/subscription-tier.md) | Optional | - | getSubscriptionTiers(): ?array | setSubscriptionTiers(?array subscriptionTiers): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Options2Builder;
use DigitalOceanApiLib\Models\Builders\SubscriptionTierBuilder;
use DigitalOceanApiLib\ApiHelper;

$options2 = Options2Builder::init()
    ->availableRegions(
        [
            'nyc3'
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
    ->build();
```



