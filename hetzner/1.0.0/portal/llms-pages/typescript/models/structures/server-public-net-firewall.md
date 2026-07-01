# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs

*This model accepts additional fields of type unknown.*


# Interface Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `number \| undefined` | Optional | ID of the Resource |
| `status` | [`Status72 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServerPublicNetFirewall, Status72 } from 'hetzner-cloud-apilib';

const serverPublicNetFirewall: ServerPublicNetFirewall = {
  id: 42,
  status: Status72.Applied,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



