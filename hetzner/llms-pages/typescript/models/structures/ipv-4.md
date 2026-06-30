# Ipv 4

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRklwdjQ

IP address (v4)


# Interface Name

`Ipv4`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `dnsPtr` | `string \| null \| undefined` | Optional | Reverse DNS PTR entry for the IPv4 address of this Load Balancer |
| `ip` | `string \| null \| undefined` | Optional | IP address (v4) of this Load Balancer |


# Example

```ts
import { Ipv4 } from 'hetzner-cloud-apilib';

const ipv4: Ipv4 = {
  dnsPtr: 'lb1.example.com',
  ip: '1.2.3.4',
};
```



