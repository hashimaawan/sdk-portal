# V2 Customers My Invoices Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `invoiceItems` | [`?(InvoiceItem[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/invoice-item.md) | Optional | - | getInvoiceItems(): ?array | setInvoiceItems(?array invoiceItems): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta.md) | Required | - | getMeta(): Meta | setMeta(Meta meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2CustomersMyInvoicesResponse1Builder;
use DigitalOceanApiLib\Models\Builders\MetaBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\InvoiceItemBuilder;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2CustomersMyInvoicesResponse1 = V2CustomersMyInvoicesResponse1Builder::init(
    MetaBuilder::init(
        6
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->invoiceItems(
        [
            InvoiceItemBuilder::init()
                ->amount('12.34')
                ->description('a56e086a317d8410c8b4cfd1f4dc9f82')
                ->duration('744')
                ->durationUnit('Hours')
                ->endTime('2020-02-01T00:00:00Z')
                ->groupDescription('my-doks-cluster')
                ->product('Kubernetes Clusters')
                ->resourceUuid('711157cb-37c8-4817-b371-44fa3504a39c')
                ->startTime('2020-01-01T00:00:00Z')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            InvoiceItemBuilder::init()
                ->amount('34.45')
                ->description('Spaces ($5/mo 250GB storage & 1TB bandwidth)')
                ->duration('744')
                ->durationUnit('Hours')
                ->endTime('2020-02-01T00:00:00Z')
                ->product('Spaces Subscription')
                ->startTime('2020-01-01T00:00:00Z')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=3&per_page=2')
                    ->next('https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=2&per_page=2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



