# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `?string` | Optional | Amount of the billing history entry. | getAmount(): ?string | setAmount(?string amount): void |
| `date` | `?DateTime` | Optional | Time the billing history entry occurred. | getDate(): ?\DateTime | setDate(?\DateTime date): void |
| `description` | `?string` | Optional | Description of the billing history entry. | getDescription(): ?string | setDescription(?string description): void |
| `invoiceId` | `?string` | Optional | ID of the invoice associated with the billing history entry, if  applicable. | getInvoiceId(): ?string | setInvoiceId(?string invoiceId): void |
| `invoiceUuid` | `?string` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. | getInvoiceUuid(): ?string | setInvoiceUuid(?string invoiceUuid): void |
| `type` | [`?string(Type6)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-6.md) | Optional | Type of billing history entry. | getType(): ?string | setType(?string type): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\BillingHistoryBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Type6;
use DigitalOceanApiLib\ApiHelper;

$billingHistory = BillingHistoryBuilder::init()
    ->amount('12.34')
    ->date(DateTimeHelper::fromRfc3339DateTime('2018-06-01T08:44:38Z'))
    ->description('Invoice for May 2018')
    ->invoiceId('123')
    ->invoiceUuid('example-uuid')
    ->type(Type6::INVOICE)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



