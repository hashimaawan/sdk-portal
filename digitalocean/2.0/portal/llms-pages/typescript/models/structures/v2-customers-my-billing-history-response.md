# V2 Customers My Billing History Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBCaWxsaW5nJTI1MjBIaXN0b3J5JTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CustomersMyBillingHistoryResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `billingHistory` | [`BillingHistory[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/billing-history.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta-1.md) | Required | Information about the response itself. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Type6,
  V2CustomersMyBillingHistoryResponse,
} from 'digitalocean-apilib';

const v2CustomersMyBillingHistoryResponse: V2CustomersMyBillingHistoryResponse = {
  meta: {
    total: 5,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  billingHistory: [
    {
      amount: '12.34',
      date: '2018-06-01T08:44:38Z',
      description: 'Invoice for May 2018',
      invoiceId: '123',
      invoiceUuid: 'example-uuid',
      type: Type6.Invoice,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      amount: '-12.34',
      date: '2018-06-02T08:44:38Z',
      description: 'Payment (MC 2018)',
      invoiceId: 'invoice_id6',
      invoiceUuid: 'invoice_uuid4',
      type: Type6.Payment,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'https://api.digitalocean.com/v2/customers/my/billing_history?page=3&per_page=2',
      next: 'https://api.digitalocean.com/v2/customers/my/billing_history?page=2&per_page=2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



