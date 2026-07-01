# Public Net 5

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlB1YmxpY05ldDU

Public Network options

*This model accepts additional fields of type unknown.*


# Interface Name

`PublicNet5`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enableIpv4` | `boolean \| undefined` | Optional | Attach an IPv4 on the public NIC. If false, no IPv4 address will be attached. Defaults to true. |
| `enableIpv6` | `boolean \| undefined` | Optional | Attach an IPv6 on the public NIC. If false, no IPv6 address will be attached. Defaults to true. |
| `ipv4` | `number \| null \| undefined` | Optional | ID of the ipv4 Primary IP to use. If omitted and enable_ipv4 is true, a new ipv4 Primary IP will automatically be created. |
| `ipv6` | `number \| null \| undefined` | Optional | ID of the ipv6 Primary IP to use. If omitted and enable_ipv6 is true, a new ipv6 Primary IP will automatically be created. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PublicNet5 } from 'hetzner-cloud-apilib';

const publicNet5: PublicNet5 = {
  enableIpv4: false,
  enableIpv6: false,
  ipv4: 42,
  ipv6: 102,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



