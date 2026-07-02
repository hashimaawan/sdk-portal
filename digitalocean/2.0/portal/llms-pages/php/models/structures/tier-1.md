# Tier 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlRpZXIx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Tier1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `allowStorageOverage` | `?bool` | Optional | A boolean indicating whether the subscription tier supports additional storage above what is included in the base plan at an additional cost per GiB used. | getAllowStorageOverage(): ?bool | setAllowStorageOverage(?bool allowStorageOverage): void |
| `includedBandwidthBytes` | `?int` | Optional | The amount of outbound data transfer included in the subscription tier in bytes. | getIncludedBandwidthBytes(): ?int | setIncludedBandwidthBytes(?int includedBandwidthBytes): void |
| `includedRepositories` | `?int` | Optional | The number of repositories included in the subscription tier. `0` indicates that the subscription tier includes unlimited repositories. | getIncludedRepositories(): ?int | setIncludedRepositories(?int includedRepositories): void |
| `includedStorageBytes` | `?int` | Optional | The amount of storage included in the subscription tier in bytes. | getIncludedStorageBytes(): ?int | setIncludedStorageBytes(?int includedStorageBytes): void |
| `monthlyPriceInCents` | `?int` | Optional | The monthly cost of the subscription tier in cents. | getMonthlyPriceInCents(): ?int | setMonthlyPriceInCents(?int monthlyPriceInCents): void |
| `name` | `?string` | Optional | The name of the subscription tier. | getName(): ?string | setName(?string name): void |
| `slug` | `?string` | Optional | The slug identifier of the subscription tier. | getSlug(): ?string | setSlug(?string slug): void |
| `storageOveragePriceInCents` | `?int` | Optional | The price paid in cents per GiB for additional storage beyond what is included in the subscription plan. | getStorageOveragePriceInCents(): ?int | setStorageOveragePriceInCents(?int storageOveragePriceInCents): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\Tier1Builder;
use DigitalOceanApiLib\ApiHelper;

$tier1 = Tier1Builder::init()
    ->allowStorageOverage(true)
    ->includedBandwidthBytes(5368709120)
    ->includedRepositories(5)
    ->includedStorageBytes(5368709120)
    ->monthlyPriceInCents(500)
    ->name('Basic')
    ->slug('basic')
    ->storageOveragePriceInCents(2)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



