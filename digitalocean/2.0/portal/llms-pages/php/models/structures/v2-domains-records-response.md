# V2 Domains Records Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEb21haW5zJTI1MjBSZWNvcmRzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DomainsRecordsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `domainRecords` | [`?(DomainRecord[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/domain-record.md) | Optional | - | getDomainRecords(): ?array | setDomainRecords(?array domainRecords): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DomainsRecordsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\DomainRecordBuilder;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2DomainsRecordsResponse = V2DomainsRecordsResponseBuilder::init(
    MetaBuilder::init(
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->domainRecords(
        [
            DomainRecordBuilder::init(
                'type8'
            )
                ->data('data2')
                ->flags(216)
                ->id(172)
                ->name('name2')
                ->port(92)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DomainRecordBuilder::init(
                'type8'
            )
                ->data('data2')
                ->flags(216)
                ->id(172)
                ->name('name2')
                ->port(92)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DomainRecordBuilder::init(
                'type8'
            )
                ->data('data2')
                ->flags(216)
                ->id(172)
                ->name('name2')
                ->port(92)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('last6')
                    ->next('next2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



