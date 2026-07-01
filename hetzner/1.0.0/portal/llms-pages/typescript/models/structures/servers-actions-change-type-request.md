# Servers Actions Change Type Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwVHlwZSUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsChangeTypeRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `serverType` | `string` | Required | ID or name of Server type the Server should migrate to |
| `upgradeDisk` | `boolean` | Required | If false, do not upgrade the disk (this allows downgrading the Server type later) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServersActionsChangeTypeRequest } from 'hetzner-cloud-apilib';

const serversActionsChangeTypeRequest: ServersActionsChangeTypeRequest = {
  serverType: 'cx11',
  upgradeDisk: true,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



