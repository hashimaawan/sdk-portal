# V2 Customers My Invoices Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBDdXN0b21lcnMlMjUyME15JTI1MjBJbnZvaWNlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2CustomersMyInvoicesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `invoiceItems` | [`InvoiceItem[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/invoice-item.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2CustomersMyInvoicesResponse1 } from 'digitalocean-apilib';

const v2CustomersMyInvoicesResponse1: V2CustomersMyInvoicesResponse1 = {
  meta: {
    total: 6,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  invoiceItems: [
    {
      amount: '12.34',
      description: 'a56e086a317d8410c8b4cfd1f4dc9f82',
      duration: '744',
      durationUnit: 'Hours',
      endTime: '2020-02-01T00:00:00Z',
      groupDescription: 'my-doks-cluster',
      product: 'Kubernetes Clusters',
      resourceUuid: '711157cb-37c8-4817-b371-44fa3504a39c',
      startTime: '2020-01-01T00:00:00Z',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      amount: '34.45',
      description: 'Spaces ($5/mo 250GB storage & 1TB bandwidth)',
      duration: '744',
      durationUnit: 'Hours',
      endTime: '2020-02-01T00:00:00Z',
      product: 'Spaces Subscription',
      startTime: '2020-01-01T00:00:00Z',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=3&per_page=2',
      next: 'https://api.digitalocean.com/v2/customers/my/invoices/22737513-0ea7-4206-8ceb-98a575af7681?page=2&per_page=2',
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



