# V2 Customers My Billing History Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCaWxsaW5nJTI1MjBIaXN0b3J5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2CustomersMyBillingHistoryResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `billingHistory` | [`?(BillingHistory[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/billing-history.md) | Optional | - | getBillingHistory(): ?array | setBillingHistory(?array billingHistory): void |
| `links` | [`?Links`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/links.md) | Optional | - | getLinks(): ?Links | setLinks(?Links links): void |
| `meta` | [`Meta1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/meta-1.md) | Required | Information about the response itself. | getMeta(): Meta1 | setMeta(Meta1 meta): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2CustomersMyBillingHistoryResponseBuilder;
use DigitalOceanApiLib\Models\Builders\Meta1Builder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\BillingHistoryBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Type6;
use DigitalOceanApiLib\Models\Builders\LinksBuilder;
use DigitalOceanApiLib\Models\Builders\PagesBuilder;

$v2CustomersMyBillingHistoryResponse = V2CustomersMyBillingHistoryResponseBuilder::init(
    Meta1Builder::init()
        ->total(5)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build()
)
    ->billingHistory(
        [
            BillingHistoryBuilder::init()
                ->amount('12.34')
                ->date(DateTimeHelper::fromRfc3339DateTime('2018-06-01T08:44:38Z'))
                ->description('Invoice for May 2018')
                ->invoiceId('123')
                ->invoiceUuid('example-uuid')
                ->type(Type6::INVOICE)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            BillingHistoryBuilder::init()
                ->amount('-12.34')
                ->date(DateTimeHelper::fromRfc3339DateTime('2018-06-02T08:44:38Z'))
                ->description('Payment (MC 2018)')
                ->invoiceId('invoice_id6')
                ->invoiceUuid('invoice_uuid4')
                ->type(Type6::PAYMENT)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->links(
        LinksBuilder::init()
            ->pages(
                PagesBuilder::init()
                    ->last('https://api.digitalocean.com/v2/customers/my/billing_history?page=3&per_page=2')
                    ->next('https://api.digitalocean.com/v2/customers/my/billing_history?page=2&per_page=2')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



