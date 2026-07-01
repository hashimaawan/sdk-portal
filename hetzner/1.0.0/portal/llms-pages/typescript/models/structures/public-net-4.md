# Public Net 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlB1YmxpY05ldDQ

Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip`

*This model accepts additional fields of type unknown.*


# Interface Name

`PublicNet4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`ServerPublicNetFirewall[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-public-net-firewall.md) | Optional | Firewalls applied to the public network interface of this Server |
| `floatingIps` | `number[]` | Required | IDs of Floating IPs assigned to this Server |
| `ipv4` | [`Ipv44 \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ipv-44.md) | Required | IP address (v4) and its reverse DNS entry of this Server |
| `ipv6` | [`Ipv64 \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ipv-64.md) | Required | IPv6 network assigned to this Server and its reverse DNS entry |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PublicNet4, Status72 } from 'hetzner-cloud-apilib';

const publicNet4: PublicNet4 = {
  floatingIps: [
    478
  ],
  ipv4: {
    blocked: false,
    dnsPtr: 'server01.example.com',
    ip: '1.2.3.4',
    id: 42,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  ipv6: {
    blocked: false,
    dnsPtr: [
      {
        dnsPtr: 'server.example.com',
        ip: '2001:db8::1',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    ip: '2001:db8::/64',
    id: 42,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  firewalls: [
    {
      id: 250,
      status: Status72.Applied,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



