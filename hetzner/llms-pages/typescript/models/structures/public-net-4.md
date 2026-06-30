# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`


# Interface Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`ServerPublicNetFirewall[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `floatingIps` | `number[]` | Required | IDs of Floating IPs assigned to this Server |
| `ipv4` | [`Ipv44 \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `ipv6` | [`Ipv64 \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |


# Example

```ts
import { PublicNet4, Status72Enum } from 'hetzner-cloud-apilib';

const publicNet4: PublicNet4 = {
  floatingIps: [
    478
  ],
  ipv4: {
    blocked: false,
    dnsPtr: 'server01.example.com',
    ip: '1.2.3.4',
    id: 42,
  },
  ipv6: {
    blocked: false,
    dnsPtr: [
      {
        dnsPtr: 'server.example.com',
        ip: '2001:db8::1',
      }
    ],
    ip: '2001:db8::/64',
    id: 42,
  },
  firewalls: [
    {
      id: 250,
      status: Status72Enum.Applied,
    }
  ],
};
```



