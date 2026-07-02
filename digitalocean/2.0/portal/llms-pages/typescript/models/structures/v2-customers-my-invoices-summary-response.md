# V2 Customers My Invoices Summary Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwU3VtbWFyeSUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CustomersMyInvoicesSummaryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `string \| undefined` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `billingPeriod` | `string \| undefined` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `creditsAndAdjustments` | [`CreditsAndAdjustments \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/credits-and-adjustments.md) | Optional | - |
| `invoiceUuid` | `string \| undefined` | Optional | UUID of the invoice |
| `overages` | [`Overages \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/overages.md) | Optional | - |
| `productCharges` | [`ProductCharges \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/product-charges.md) | Optional | - |
| `taxes` | [`Taxes \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/taxes.md) | Optional | - |
| `userBillingAddress` | [`UserBillingAddress \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/user-billing-address.md) | Optional | - |
| `userCompany` | `string \| undefined` | Optional | Company of the DigitalOcean customer being invoiced, if set. |
| `userEmail` | `string \| undefined` | Optional | Email of the DigitalOcean customer being invoiced. |
| `userName` | `string \| undefined` | Optional | Name of the DigitalOcean customer being invoiced. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CustomersMyInvoicesSummaryResponse } from 'digitalocean-apilib';

const v2CustomersMyInvoicesSummaryResponse: V2CustomersMyInvoicesSummaryResponse = {
  amount: '27.13',
  billingPeriod: '2020-01',
  creditsAndAdjustments: {
    amount: 'amount6',
    name: 'name4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  invoiceUuid: '22737513-0ea7-4206-8ceb-98a575af7681',
  overages: {
    amount: 'amount6',
    name: 'name4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  userCompany: 'DigitalOcean',
  userEmail: 'sammy@digitalocean.com',
  userName: 'Sammy Shark',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



