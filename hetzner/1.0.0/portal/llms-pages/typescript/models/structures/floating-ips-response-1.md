# Floating Ips Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkZsb2F0aW5nJTI1MjBJcHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type unknown.*


# Interface Name

`FloatingIpsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Optional | - |
| `floatingIp` | [`FloatingIp`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/floating-ip.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { FloatingIpsResponse1, Status, Type16 } from 'hetzner-cloud-apilib';

const floatingIpsResponse1: FloatingIpsResponse1 = {
  floatingIp: {
    blocked: false,
    created: '2016-01-30T23:55:00+00:00',
    description: 'this describes my resource',
    dnsPtr: [
      {
        dnsPtr: 'server.example.com',
        ip: '2001:db8::1',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
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
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
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
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    server: 42,
    type: Type16.Ipv4,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  action: {
    command: 'command6',
    error: {
      code: 'code2',
      message: 'message4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    finished: 'finished0',
    id: 238,
    progress: 143.26,
    resources: [
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        id: 198,
        type: 'type0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    started: 'started8',
    status: Status.Running,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



