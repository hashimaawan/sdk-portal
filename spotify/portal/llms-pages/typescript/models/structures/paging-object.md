# Paging Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/spotify/#/typescript/x-redirect/JTI0bSUyRlBhZ2luZ09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`PagingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string` | Required | A link to the Web API endpoint returning the full result of the request |
| `limit` | `number` | Required | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| null` | Required | URL to the next page of items. ( `null` if none) |
| `offset` | `number` | Required | The offset of the items returned (as set in the query or by default) |
| `previous` | `string \| null` | Required | URL to the previous page of items. ( `null` if none) |
| `total` | `number` | Required | The total number of items available to return. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  PagingObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const pagingObject: PagingObject = {
  href: 'https://api.spotify.com/v1/me/shows?offset=0&limit=20\n',
  limit: 20,
  next: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  offset: 0,
  previous: 'https://api.spotify.com/v1/me/shows?offset=1&limit=1',
  total: 4,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



