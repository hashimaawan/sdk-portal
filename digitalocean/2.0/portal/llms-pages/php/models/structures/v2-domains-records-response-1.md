# V2 Domains Records Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DomainsRecordsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `domainRecord` | [`?DomainRecord`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/domain-record.md) | Optional | - | getDomainRecord(): ?DomainRecord | setDomainRecord(?DomainRecord domainRecord): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DomainsRecordsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\DomainRecordBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2DomainsRecordsResponse1 = V2DomainsRecordsResponse1Builder::init()
    ->domainRecord(
        DomainRecordBuilder::init(
            'A'
        )
            ->data('162.10.66.0')
            ->flags(null)
            ->id(28448433)
            ->name('www')
            ->port(null)
            ->priority(null)
            ->tag(null)
            ->ttl(1800)
            ->weight(null)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



