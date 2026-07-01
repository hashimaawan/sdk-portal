# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `aliasIps` | `string[]` | Required | New alias IPs to set for this Server |
| `network` | `number` | Required | ID of an existing Network already attached to the Server |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServersActionsChangeAliasIpsRequest } from 'hetzner-cloud-apilib';

const serversActionsChangeAliasIpsRequest: ServersActionsChangeAliasIpsRequest = {
  aliasIps: [
    '10.0.1.2'
  ],
  network: 4711,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



