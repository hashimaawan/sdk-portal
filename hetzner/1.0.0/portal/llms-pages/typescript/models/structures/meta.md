# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type unknown.*


# Interface Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/pagination.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Meta } from 'hetzner-cloud-apilib';

const meta: Meta = {
  pagination: {
    lastPage: 4,
    nextPage: 4,
    page: 3,
    perPage: 25,
    previousPage: 2,
    totalEntries: 100,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



