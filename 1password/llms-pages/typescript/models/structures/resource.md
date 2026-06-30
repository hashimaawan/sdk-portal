# Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlJlc291cmNl

*This model accepts additional fields of type unknown.*


# Interface Name

`Resource`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item` | [`Item2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/item-2.md) | Optional | - |
| `itemVersion` | `number \| undefined` | Optional | - |
| `type` | [`Type \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/type.md) | Optional | - |
| `vault` | [`Vault3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/vault-3.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Resource, Type } from 'm-1-password-connectlib';

const resource: Resource = {
  item: {
    id: 'id2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  itemVersion: 108,
  type: Type.Item,
  vault: {
    id: 'id6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



