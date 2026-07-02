# Invoice Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkludm9pY2VJdGVt

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`InvoiceItem`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `string \| undefined` | Optional | Billed amount of this invoice item. Billed in USD. |
| `description` | `string \| undefined` | Optional | Description of the invoice item. |
| `duration` | `string \| undefined` | Optional | Duration of time this invoice item was used and subsequently billed. |
| `durationUnit` | `string \| undefined` | Optional | Unit of time for duration. |
| `endTime` | `string \| undefined` | Optional | Time the invoice item stopped being billed for usage. |
| `groupDescription` | `string \| undefined` | Optional | Description of the invoice item when it is a grouped set of usage, such  as DOKS or databases. |
| `product` | `string \| undefined` | Optional | Name of the product being billed in the invoice item. |
| `projectName` | `string \| undefined` | Optional | Name of the DigitalOcean Project this resource belongs to. |
| `resourceId` | `string \| undefined` | Optional | ID of the resource billing in the invoice item if available. |
| `resourceUuid` | `string \| undefined` | Optional | UUID of the resource billing in the invoice item if available. |
| `startTime` | `string \| undefined` | Optional | Time the invoice item began to be billed for usage. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { InvoiceItem } from 'digitalocean-apilib';

const invoiceItem: InvoiceItem = {
  amount: '12.34',
  description: 'a56e086a317d8410c8b4cfd1f4dc9f82',
  duration: '744',
  durationUnit: 'Hours',
  endTime: '2020-02-01T00:00:00Z',
  groupDescription: 'my-doks-cluster',
  product: 'Kubernetes Clusters',
  projectName: 'web',
  resourceId: '2353624',
  resourceUuid: '711157cb-37c8-4817-b371-44fa3504a39c',
  startTime: '2020-01-01T00:00:00Z',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



