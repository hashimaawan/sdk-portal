# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlBhZ2luYXRpb24


# Interface Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `lastPage` | `number \| null` | Required | ID of the last page available. Can be null if the current page is the last one. |
| `nextPage` | `number \| null` | Required | ID of the next page. Can be null if the current page is the last one. |
| `page` | `number` | Required | Current page number |
| `perPage` | `number` | Required | Maximum number of items shown per page in the response |
| `previousPage` | `number \| null` | Required | ID of the previous page. Can be null if the current page is the first one. |
| `totalEntries` | `number \| null` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. |


# Example

```ts
import { Pagination } from 'hetzner-cloud-apilib';

const pagination: Pagination = {
  lastPage: 4,
  nextPage: 4,
  page: 3,
  perPage: 25,
  previousPage: 2,
  totalEntries: 100,
};
```



