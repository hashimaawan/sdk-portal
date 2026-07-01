# Ipv 44

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRklwdjQ0

IP address (v4) and its reverse DNS entry of this Server


# Interface Name

`Ipv44`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `boolean` | Required | If the IP is blocked by our anti abuse dept |
| `dnsPtr` | `string` | Required | Reverse DNS PTR entry for the IPv4 addresses of this Server |
| `id` | `number \| undefined` | Optional | ID of the Resource |
| `ip` | `string` | Required | IP address (v4) of this Server |


# Example

```ts
import { Ipv44 } from 'hetzner-cloud-apilib';

const ipv44: Ipv44 = {
  blocked: false,
  dnsPtr: 'server01.example.com',
  ip: '1.2.3.4',
  id: 42,
};
```



