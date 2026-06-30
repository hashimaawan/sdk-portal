# Copyright Object

Source: https://github.com/hashimaawan/sdk-portal/tree/main/spotify/#/typescript/x-redirect/JTI0bSUyRkNvcHlyaWdodE9iamVjdA

*This model accepts additional fields of type unknown.*


# Interface Name

`CopyrightObject`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `text` | `string \| undefined` | Optional | The copyright text for this content. |
| `type` | `string \| undefined` | Optional | The type of copyright: `C` = the copyright, `P` = the sound recording (performance) copyright. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CopyrightObject,
} from 'spotify-web-api-with-fixes-and-improvements-from-sonalluxlib';

const copyrightObject: CopyrightObject = {
  text: 'text4',
  type: 'type4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



