# Item

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/typescript/x-redirect/JTI0bSUyRkl0ZW0

*This model accepts additional fields of type unknown.*


# Interface Name

`Item`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `category` | [`Category`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/category.md) | Required | - |
| `createdAt` | `string \| undefined` | Optional, Read-only | - |
| `favorite` | `boolean \| undefined` | Optional | **Default**: `false` |
| `id` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `^[\da-z]{26}$` |
| `lastEditedBy` | `string \| undefined` | Optional, Read-only | - |
| `state` | [`State \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/enumerations/state.md) | Optional, Read-only | - |
| `tags` | `string[] \| undefined` | Optional | - |
| `title` | `string \| undefined` | Optional | - |
| `updatedAt` | `string \| undefined` | Optional, Read-only | - |
| `urls` | [`Url[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/url.md) | Optional | - |
| `vault` | [`Vault1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/llms-pages/typescript/models/structures/vault-1.md) | Required | - |
| `version` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Category, Item, State } from 'm-1-password-connectlib';

const item: Item = {
  category: Category.SshKey,
  vault: {
    id: 'id6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  createdAt: '2016-03-13T12:52:32.123Z',
  favorite: false,
  id: 'id2',
  lastEditedBy: 'lastEditedBy8',
  state: State.Archived,
  urls: [
    {
      href: 'https://example.com',
      primary: true,
    },
    {
      href: 'https://example.org',
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



