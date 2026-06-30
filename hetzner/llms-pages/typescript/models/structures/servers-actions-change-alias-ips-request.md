# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA


# Interface Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `aliasIps` | `string[]` | Required | New alias IPs to set for this Server |
| `network` | `number` | Required | ID of an existing Network already attached to the Server |


# Example

```ts
import { ServersActionsChangeAliasIpsRequest } from 'hetzner-cloud-apilib';

const serversActionsChangeAliasIpsRequest: ServersActionsChangeAliasIpsRequest = {
  aliasIps: [
    '10.0.1.2'
  ],
  network: 4711,
};
```



