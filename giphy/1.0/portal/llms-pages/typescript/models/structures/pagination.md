# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/typescript/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.

*This model accepts additional fields of type unknown.*


# Interface Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `number \| undefined` | Optional | Total number of items returned. |
| `offset` | `number \| undefined` | Optional | Position in pagination. |
| `totalCount` | `number \| undefined` | Optional | Total number of items available. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Pagination } from 'giphy-apilib';

const pagination: Pagination = {
  count: 25,
  offset: 75,
  totalCount: 250,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



