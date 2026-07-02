# Invoice Preview

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkludm9pY2VQcmV2aWV3

The invoice preview.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`InvoicePreview`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `string \| undefined` | Optional | Total amount of the invoice, in USD.  This will reflect month-to-date usage in the invoice preview. |
| `invoicePeriod` | `string \| undefined` | Optional | Billing period of usage for which the invoice is issued, in `YYYY-MM`  format. |
| `invoiceUuid` | `string \| undefined` | Optional | The UUID of the invoice. The canonical reference for the invoice. |
| `updatedAt` | `string \| undefined` | Optional | Time the invoice was last updated.  This is only included with the invoice preview. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { InvoicePreview } from 'digitalocean-apilib';

const invoicePreview: InvoicePreview = {
  amount: '23.45',
  invoicePeriod: '2020-01',
  invoiceUuid: 'fdabb512-6faf-443c-ba2e-665452332a9e',
  updatedAt: '2020-01-23T06:31:50Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



