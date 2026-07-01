# Public Net

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlB1YmxpY05ldA

Public network information

*This model accepts additional fields of type unknown.*


# Interface Name

`PublicNet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enabled` | `boolean` | Required | Public Interface enabled or not |
| `ipv4` | [`Ipv4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ipv-4.md) | Required | IP address (v4) |
| `ipv6` | [`Ipv6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/ipv-6.md) | Required | IP address (v6) |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PublicNet } from 'hetzner-cloud-apilib';

const publicNet: PublicNet = {
  enabled: false,
  ipv4: {
    dnsPtr: 'lb1.example.com',
    ip: '1.2.3.4',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  ipv6: {
    dnsPtr: 'lb1.example.com',
    ip: '2001:db8::1',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



