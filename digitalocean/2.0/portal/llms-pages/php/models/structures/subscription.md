# Subscription

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlN1YnNjcmlwdGlvbg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Subscription`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?DateTime` | Optional, Read-only | The time at which the subscription was created. | getCreatedAt(): ?\DateTime | setCreatedAt(?\DateTime createdAt): void |
| `tier` | [`?Tier1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/tier-1.md) | Optional | - | getTier(): ?Tier1 | setTier(?Tier1 tier): void |
| `updatedAt` | `?DateTime` | Optional, Read-only | The time at which the subscription was last updated. | getUpdatedAt(): ?\DateTime | setUpdatedAt(?\DateTime updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\SubscriptionBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Tier1Builder;
use DigitalOceanApiLib\ApiHelper;

$subscription = SubscriptionBuilder::init()
    ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-01-23T21:19:12Z'))
    ->tier(
        Tier1Builder::init()
            ->allowStorageOverage(false)
            ->includedBandwidthBytes(46)
            ->includedRepositories(68)
            ->includedStorageBytes(112)
            ->monthlyPriceInCents(110)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->updatedAt(DateTimeHelper::fromRfc3339DateTime('2020-11-05T15:53:24Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



