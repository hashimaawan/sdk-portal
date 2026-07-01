# Server 11

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcjEx

*This model accepts additional fields of type unknown.*


# Interface Name

`Server11`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number` | Required | ID of the Server |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { Server11 } from 'hetzner-cloud-apilib';

const server11: Server11 = {
  id: 85,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



