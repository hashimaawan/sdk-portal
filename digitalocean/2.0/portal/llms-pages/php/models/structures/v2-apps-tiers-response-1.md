# V2 Apps Tiers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tier` | [`?Tier`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/tier.md) | Optional | - | getTier(): ?Tier | setTier(?Tier tier): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsTiersResponse1Builder;
use DigitalOceanApiLib\Models\Builders\TierBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsTiersResponse1 = V2AppsTiersResponse1Builder::init()
    ->tier(
        TierBuilder::init()
            ->buildSeconds('build_seconds0')
            ->egressBandwidthBytes('egress_bandwidth_bytes6')
            ->name('name2')
            ->slug('slug4')
            ->storageBytes('storage_bytes0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



