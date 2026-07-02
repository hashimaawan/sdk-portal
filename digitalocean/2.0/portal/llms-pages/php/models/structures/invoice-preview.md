# Invoice Preview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkludm9pY2VQcmV2aWV3

The invoice preview.

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`InvoicePreview`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `?string` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. | getAmount(): ?string | setAmount(?string amount): void |
| `invoicePeriod` | `?string` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. | getInvoicePeriod(): ?string | setInvoicePeriod(?string invoicePeriod): void |
| `invoiceUuid` | `?string` | Optional | The UUID of the invoice. The canonical reference for the invoice. | getInvoiceUuid(): ?string | setInvoiceUuid(?string invoiceUuid): void |
| `updatedAt` | `?string` | Optional | Time the invoice was last updated.  This is only included with the invoice preview. | getUpdatedAt(): ?string | setUpdatedAt(?string updatedAt): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\InvoicePreviewBuilder;
use DigitalOceanApiLib\ApiHelper;

$invoicePreview = InvoicePreviewBuilder::init()
    ->amount('23.45')
    ->invoicePeriod('2020-01')
    ->invoiceUuid('fdabb512-6faf-443c-ba2e-665452332a9e')
    ->updatedAt('2020-01-23T06:31:50Z')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



