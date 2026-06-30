# Vault

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRlZhdWx0

*This model accepts additional fields of type unknown.*


# Interface Name

`Vault`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attributeVersion` | `number \| undefined` | Optional | The vault version |
| `contentVersion` | `number \| undefined` | Optional | The version of the vault contents |
| `createdAt` | `string \| undefined` | Optional, Read-only | - |
| `description` | `string \| undefined` | Optional | - |
| `id` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `items` | `number \| undefined` | Optional | Number of active items in the vault |
| `name` | `string \| undefined` | Optional | - |
| `type` | [`Type2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/type-2.md) | Optional | - |
| `updatedAt` | `string \| undefined` | Optional, Read-only | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Vault } from 'm-1-password-connectlib';

const vault: Vault = {
  attributeVersion: 108,
  contentVersion: 228,
  createdAt: '2016-03-13T12:52:32.123Z',
  description: 'description6',
  id: 'id6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



