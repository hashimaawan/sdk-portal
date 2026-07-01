# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRuc1B0cg

*This model accepts additional fields of type unknown.*


# Interface Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `ip` | `string` | Required | Single IPv4 or IPv6 address |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { DnsPtr } from 'hetzner-cloud-apilib';

const dnsPtr: DnsPtr = {
  dnsPtr: 'server.example.com',
  ip: '2001:db8::1',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



