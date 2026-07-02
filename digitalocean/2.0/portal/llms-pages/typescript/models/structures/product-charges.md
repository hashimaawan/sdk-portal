# Product Charges

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlByb2R1Y3RDaGFyZ2Vz

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`ProductCharges`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount` | `string \| undefined` | Optional | Total amount charged |
| `items` | [`Item[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/item.md) | Optional | List of amount, and grouped aggregates by resource type. |
| `name` | `string \| undefined` | Optional | Description of usage charges |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { ProductCharges } from 'digitalocean-apilib';

const productCharges: ProductCharges = {
  amount: '12.34',
  items: [
    {
      amount: '10.00',
      count: '1',
      name: 'Spaces Subscription',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      amount: '2.34',
      count: '1',
      name: 'Database Clusters',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  name: 'Product usage charges',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



