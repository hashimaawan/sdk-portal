# Patch

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlBhdGNo

*This model accepts additional fields of type unknown.*


# Interface Name

`Patch`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `op` | [`Op`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/op.md) | Required | - |
| `path` | `string` | Required | An RFC6901 JSON Pointer pointing to the Item document, an Item Attribute, and Item Field by Field ID, or an Item Field Attribute |
| `value` | `unknown \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Op, Patch } from 'm-1-password-connectlib';

const patch: Patch = {
  op: Op.Remove,
  path: '/fields/06gnn2b95example10q91512p5/label',
  value: { 'key1': 'val1', 'key2': 'val2' },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



