# Floating Ips Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMg


# Interface Name

`FloatingIpsResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `floatingIp` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/floating-ip.md) | Required | - |


# Example

```ts
import { FloatingIpsResponse2, Type16Enum } from 'hetzner-cloud-apilib';

const floatingIpsResponse2: FloatingIpsResponse2 = {
  floatingIp: {
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
      'key0': 'labels4',
      'key1': 'labels3',
      'key2': 'labels2'
    },
    name: 'my-resource',
    protection: {
      mDelete: false,
    },
    server: 42,
    type: Type16Enum.Ipv4,
  },
};
```



