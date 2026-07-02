# V2 Customers My Invoices Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CustomersMyInvoicesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoicePreview` | [`InvoicePreview \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/invoice-preview.md) | Optional | The invoice preview. |
| `invoices` | [`InvoicePreview[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/invoice-preview.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CustomersMyInvoicesResponse } from 'digitalocean-apilib';

const v2CustomersMyInvoicesResponse: V2CustomersMyInvoicesResponse = {
  meta: {
    total: 70,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  invoicePreview: {
    amount: '34.56',
    invoicePeriod: '2020-02',
    invoiceUuid: '1afe95e6-0958-4eb0-8d9a-9c5060d3ef03',
    updatedAt: '2020-02-23T06:31:50Z',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  invoices: [
    {
      amount: '12.34',
      invoicePeriod: '2019-12',
      invoiceUuid: '22737513-0ea7-4206-8ceb-98a575af7681',
      updatedAt: 'updated_at8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      amount: '23.45',
      invoicePeriod: '2019-11',
      invoiceUuid: 'fdabb512-6faf-443c-ba2e-665452332a9e',
      updatedAt: 'updated_at8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'https://api.digitalocean.com/v2/customers/my/invoices?page=35&per_page=2',
      next: 'https://api.digitalocean.com/v2/customers/my/invoices?page=2&per_page=2',
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



