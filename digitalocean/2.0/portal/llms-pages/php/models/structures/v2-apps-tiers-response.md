# V2 Apps Tiers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsTiersResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tiers` | [`?(Tier[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/tier.md) | Optional | - | getTiers(): ?array | setTiers(?array tiers): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsTiersResponseBuilder;
use DigitalOceanApiLib\Models\Builders\TierBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsTiersResponse = V2AppsTiersResponseBuilder::init()
    ->tiers(
        [
            TierBuilder::init()
                ->buildSeconds('build_seconds4')
                ->egressBandwidthBytes('egress_bandwidth_bytes2')
                ->name('name8')
                ->slug('slug8')
                ->storageBytes('storage_bytes4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TierBuilder::init()
                ->buildSeconds('build_seconds4')
                ->egressBandwidthBytes('egress_bandwidth_bytes2')
                ->name('name8')
                ->slug('slug8')
                ->storageBytes('storage_bytes4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TierBuilder::init()
                ->buildSeconds('build_seconds4')
                ->egressBandwidthBytes('egress_bandwidth_bytes2')
                ->name('name8')
                ->slug('slug8')
                ->storageBytes('storage_bytes4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



