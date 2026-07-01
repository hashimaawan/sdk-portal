# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information


# Interface Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean` | Required | Public Interface enabled or not |
| `ipv4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ipv-4.md) | Required | IP address (v4) |
| `ipv6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ipv-6.md) | Required | IP address (v6) |


# Example

```ts
import { PublicNet } from 'hetzner-cloud-apilib';

const publicNet: PublicNet = {
  enabled: false,
  ipv4: {
    dnsPtr: 'lb1.example.com',
    ip: '1.2.3.4',
  },
  ipv6: {
    dnsPtr: 'lb1.example.com',
    ip: '2001:db8::1',
  },
};
```



