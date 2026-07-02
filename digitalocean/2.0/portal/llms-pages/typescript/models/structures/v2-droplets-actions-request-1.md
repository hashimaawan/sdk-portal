# V2 Droplets Actions Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2DropletsActionsRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. |
| `name` | `string \| undefined` | Optional | The name to give the new snapshot of the Droplet. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Type12, V2DropletsActionsRequest1 } from 'digitalocean-apilib';

const v2DropletsActionsRequest1: V2DropletsActionsRequest1 = {
  type: Type12.Reboot,
  name: 'Nifty New Snapshot',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



