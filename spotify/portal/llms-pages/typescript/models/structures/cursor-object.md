# Cursor Object

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/typescript/x-redirect/JTI0bSUyRkN1cnNvck9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CursorObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `after` | `string \| undefined` | Optional | The cursor to use as key to find the next page of items. |
| `before` | `string \| undefined` | Optional | The cursor to use as key to find the previous page of items. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CursorObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const cursorObject: CursorObject = {
  after: 'after0',
  before: 'before8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



