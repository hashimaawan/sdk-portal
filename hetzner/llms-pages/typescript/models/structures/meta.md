# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRk1ldGE


# Interface Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/pagination.md) | Required | - |


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
  },
};
```



