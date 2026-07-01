# Ipv 6

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRklwdjY

IP address (v6)


# Interface Name

`Ipv6`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string \| null \| undefined` | Optional | Reverse DNS PTR entry for the IPv6 address of this Load Balancer |
| `ip` | `string \| null \| undefined` | Optional | IP address (v6) of this Load Balancer |


# Example

```ts
import { Ipv6 } from 'hetzner-cloud-apilib';

const ipv6: Ipv6 = {
  dnsPtr: 'lb1.example.com',
  ip: '2001:db8::1',
};
```



