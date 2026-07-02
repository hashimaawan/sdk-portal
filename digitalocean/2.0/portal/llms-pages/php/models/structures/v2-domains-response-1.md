# V2 Domains Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DomainsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `domain` | [`?Domain1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/domain-1.md) | Optional | - | getDomain(): ?Domain1 | setDomain(?Domain1 domain): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DomainsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\Domain1Builder;
use DigitalOceanApiLib\ApiHelper;

$v2DomainsResponse1 = V2DomainsResponse1Builder::init()
    ->domain(
        Domain1Builder::init()
            ->ipAddress('ip_address6')
            ->name('example.com')
            ->ttl(1800)
            ->zoneFile(null)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



