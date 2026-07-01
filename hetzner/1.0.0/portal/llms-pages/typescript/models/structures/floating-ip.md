# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA


# Interface Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blocked` | `boolean` | Required | Whether the IP is blocked |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `description` | `string \| null` | Required | Description of the Resource |
| `dnsPtr` | [`DnsPtr[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `homeLocation` | [`HomeLocation`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/home-location.md) | Required | Location the Floating IP was created in. Routing is optimized for this Location. |
| `id` | `number` | Required | ID of the Resource |
| `ip` | `string` | Required | IP address |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `server` | `number \| null` | Required | ID of the Server the Floating IP is assigned to, null if it is not assigned at all |
| `type` | [`Type16Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-16.md) | Required | Type of the Floating IP |


# Example

```ts
import { FloatingIp, Type16Enum } from 'hetzner-cloud-apilib';

const floatingIp: FloatingIp = {
  blocked: false,
  created: '2016-01-30T23:55:00+00:00',
  description: 'this describes my resource',
  dnsPtr: [
    {
      dnsPtr: 'server.example.com',
      ip: '2001:db8::1',
    }
  ],
  homeLocation: {
    city: 'Falkenstein',
    country: 'DE',
    description: 'Falkenstein DC Park 1',
    id: 1,
    latitude: 50.47612,
    longitude: 12.370071,
    name: 'fsn1',
    networkZone: 'eu-central',
  },
  id: 42,
  ip: '131.232.99.1',
  labels: {
    'key0': 'labels6'
  },
  name: 'my-resource',
  protection: {
    mDelete: false,
  },
  server: 42,
  type: Type16Enum.Ipv4,
};
```



