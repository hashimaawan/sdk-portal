# Billing History

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkJpbGxpbmdIaXN0b3J5

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`BillingHistory`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `string \| undefined` | Optional | Amount of the billing history entry. |
| `date` | `string \| undefined` | Optional | Time the billing history entry occurred. |
| `description` | `string \| undefined` | Optional | Description of the billing history entry. |
| `invoiceId` | `string \| undefined` | Optional | ID of the invoice associated with the billing history entry, if  applicable. |
| `invoiceUuid` | `string \| undefined` | Optional | UUID of the invoice associated with the billing history entry, if  applicable. |
| `type` | [`Type6 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-6.md) | Optional | Type of billing history entry. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { BillingHistory, Type6 } from 'digitalocean-apilib';

const billingHistory: BillingHistory = {
  amount: '12.34',
  date: '2018-06-01T08:44:38Z',
  description: 'Invoice for May 2018',
  invoiceId: '123',
  invoiceUuid: 'example-uuid',
  type: Type6.Invoice,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



