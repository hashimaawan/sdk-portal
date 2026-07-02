# Tier

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlRpZXI

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Tier`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `buildSeconds` | `?string` | Optional | - | getBuildSeconds(): ?string | setBuildSeconds(?string buildSeconds): void |
| `egressBandwidthBytes` | `?string` | Optional | - | getEgressBandwidthBytes(): ?string | setEgressBandwidthBytes(?string egressBandwidthBytes): void |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `slug` | `?string` | Optional | - | getSlug(): ?string | setSlug(?string slug): void |
| `storageBytes` | `?string` | Optional | - | getStorageBytes(): ?string | setStorageBytes(?string storageBytes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\TierBuilder;
use DigitalOceanApiLib\ApiHelper;

$tier = TierBuilder::init()
    ->buildSeconds('233')
    ->egressBandwidthBytes('123')
    ->name('test')
    ->slug('test')
    ->storageBytes('10000000')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



