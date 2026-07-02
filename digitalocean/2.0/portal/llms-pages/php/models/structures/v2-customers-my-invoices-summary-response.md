# V2 Customers My Invoices Summary Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwU3VtbWFyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2CustomersMyInvoicesSummaryResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `amount` | `?string` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. | getAmount(): ?string | setAmount(?string amount): void |
| `billingPeriod` | `?string` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. | getBillingPeriod(): ?string | setBillingPeriod(?string billingPeriod): void |
| `creditsAndAdjustments` | [`?CreditsAndAdjustments`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/credits-and-adjustments.md) | Optional | - | getCreditsAndAdjustments(): ?CreditsAndAdjustments | setCreditsAndAdjustments(?CreditsAndAdjustments creditsAndAdjustments): void |
| `invoiceUuid` | `?string` | Optional | UUID of the invoice | getInvoiceUuid(): ?string | setInvoiceUuid(?string invoiceUuid): void |
| `overages` | [`?Overages`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/overages.md) | Optional | - | getOverages(): ?Overages | setOverages(?Overages overages): void |
| `productCharges` | [`?ProductCharges`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/product-charges.md) | Optional | - | getProductCharges(): ?ProductCharges | setProductCharges(?ProductCharges productCharges): void |
| `taxes` | [`?Taxes`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/taxes.md) | Optional | - | getTaxes(): ?Taxes | setTaxes(?Taxes taxes): void |
| `userBillingAddress` | [`?UserBillingAddress`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/user-billing-address.md) | Optional | - | getUserBillingAddress(): ?UserBillingAddress | setUserBillingAddress(?UserBillingAddress userBillingAddress): void |
| `userCompany` | `?string` | Optional | Company of the DigitalOcean customer being invoiced, if set. | getUserCompany(): ?string | setUserCompany(?string userCompany): void |
| `userEmail` | `?string` | Optional | Email of the DigitalOcean customer being invoiced. | getUserEmail(): ?string | setUserEmail(?string userEmail): void |
| `userName` | `?string` | Optional | Name of the DigitalOcean customer being invoiced. | getUserName(): ?string | setUserName(?string userName): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2CustomersMyInvoicesSummaryResponseBuilder;
use DigitalOceanApiLib\Models\Builders\CreditsAndAdjustmentsBuilder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\OveragesBuilder;

$v2CustomersMyInvoicesSummaryResponse = V2CustomersMyInvoicesSummaryResponseBuilder::init()
    ->amount('27.13')
    ->billingPeriod('2020-01')
    ->creditsAndAdjustments(
        CreditsAndAdjustmentsBuilder::init()
            ->amount('amount6')
            ->name('name4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->invoiceUuid('22737513-0ea7-4206-8ceb-98a575af7681')
    ->overages(
        OveragesBuilder::init()
            ->amount('amount6')
            ->name('name4')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->userCompany('DigitalOcean')
    ->userEmail('sammy@digitalocean.com')
    ->userName('Sammy Shark')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



