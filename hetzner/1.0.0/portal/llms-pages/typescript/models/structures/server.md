# Server

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcg

*This model accepts additional fields of type unknown.*


# Interface Name

`Server`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Resource |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Server } from 'hetzner-cloud-apilib';

const server: Server = {
  id: 42,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



