# Dns Ptr

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRuc1B0cg


# Interface Name

`DnsPtr`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `ip` | `string` | Required | Single IPv4 or IPv6 address |


# Example

```ts
import { DnsPtr } from 'hetzner-cloud-apilib';

const dnsPtr: DnsPtr = {
  dnsPtr: 'server.example.com',
  ip: '2001:db8::1',
};
```



