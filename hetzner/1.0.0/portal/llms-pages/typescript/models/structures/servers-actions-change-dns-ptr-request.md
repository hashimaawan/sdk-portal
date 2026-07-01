# Servers Actions Change Dns Ptr Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwRG5zJTI1MjBQdHIlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type unknown.*


# Interface Name

`ServersActionsChangeDnsPtrRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string \| null` | Required | Hostname to set as a reverse DNS PTR entry, reset to original value if `null` |
| `ip` | `string` | Required | Primary IP address for which the reverse DNS entry should be set |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ServersActionsChangeDnsPtrRequest } from 'hetzner-cloud-apilib';

const serversActionsChangeDnsPtrRequest: ServersActionsChangeDnsPtrRequest = {
  dnsPtr: 'server01.example.com',
  ip: '1.2.3.4',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



