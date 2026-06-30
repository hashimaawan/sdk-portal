# Cursor Paging Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkN1cnNvclBhZ2luZ09iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CursorPagingObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `string \| undefined` | Optional | A link to the Web API endpoint returning the full result of the request. |
| `limit` | `number \| undefined` | Optional | The maximum number of items in the response (as set in the query or by default). |
| `next` | `string \| undefined` | Optional | URL to the next page of items. ( `null` if none) |
| `cursors` | [`CursorObject \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/llms-pages/typescript/models/structures/cursor-object.md) | Optional | The cursors used to find the next set of items. |
| `total` | `number \| undefined` | Optional | The total number of items available to return. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CursorPagingObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const cursorPagingObject: CursorPagingObject = {
  href: 'href8',
  limit: 82,
  next: 'next6',
  cursors: {
    after: 'after8',
    before: 'before6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  total: 176,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



