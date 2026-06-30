# Ipv 64

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRklwdjY0

IPv6 network assigned to this Server and its reverse DNS entry


# Interface Name

`Ipv64`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `boolean` | Required | If the IP is blocked by our anti abuse dept |
| `dnsPtr` | [`DnsPtr8[] \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/dns-ptr-8.md) | Required | Reverse DNS PTR entries for the IPv6 addresses of this Server, `null` by default |
| `id` | `number \| undefined` | Optional | ID of the Resource |
| `ip` | `string` | Required | IP address (v6) of this Server |


# Example

```ts
import { Ipv64 } from 'hetzner-cloud-apilib';

const ipv64: Ipv64 = {
  blocked: false,
  dnsPtr: [
    {
      dnsPtr: 'server.example.com',
      ip: '2001:db8::1',
    }
  ],
  ip: '2001:db8::/64',
  id: 42,
};
```



