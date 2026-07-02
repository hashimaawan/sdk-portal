# Pending Change

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlBlbmRpbmdDaGFuZ2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`PendingChange`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dropletId` | `number \| undefined` | Optional | - |
| `removing` | `boolean \| undefined` | Optional | - |
| `status` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { PendingChange } from 'digitalocean-apilib';

const pendingChange: PendingChange = {
  dropletId: 8043964,
  removing: false,
  status: 'waiting',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



