# Dns Ptr 8

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkRuc1B0cjg


# Interface Name

`DnsPtr8`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string` | Required | DNS pointer for the specific IP address |
| `ip` | `string` | Required | Single IPv6 address of this Server for which the reverse DNS entry has been set up |


# Example

```ts
import { DnsPtr8 } from 'hetzner-cloud-apilib';

const dnsPtr8: DnsPtr8 = {
  dnsPtr: 'server.example.com',
  ip: '2001:db8::1',
};
```



