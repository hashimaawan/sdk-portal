# Primary IP 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaW1hcnlJUDE

*This model accepts additional fields of type unknown.*


# Interface Name

`PrimaryIp1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `assigneeId` | `number \| null` | Required | ID of the resource the Primary IP is assigned to, null if it is not assigned at all |
| `assigneeType` | `string` | Required, Constant | Resource type the Primary IP can be assigned to<br><br>**Value**: `'server'` |
| `autoDelete` | `boolean` | Required | Delete this Primary IP when the resource it is assigned to is deleted |
| `blocked` | `boolean` | Required | Whether the IP is blocked |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/datacenter-2.md) | Required | Datacenter this Primary IP is located at |
| `dnsPtr` | [`DnsPtr[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/dns-ptr.md) | Required | Array of reverse DNS entries |
| `id` | `number` | Required | ID of the Resource |
| `ip` | `string` | Required | IP address |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `type` | [`Type50`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/type-50.md) | Required | Type of the Primary IP |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PrimaryIp1, Type50 } from 'hetzner-cloud-apilib';

const primaryIp1: PrimaryIp1 = {
  assigneeId: 17,
  assigneeType: 'server',
  autoDelete: true,
  blocked: false,
  created: '2016-01-30T23:55:00+00:00',
  datacenter: {
    description: 'Falkenstein DC Park 8',
    id: 42,
    location: {
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
    name: 'fsn1-dc8',
    serverTypes: {
      available: [
        1,
        2,
        3
      ],
      availableForMigration: [
        1,
        2,
        3
      ],
      supported: [
        1,
        2,
        3
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  dnsPtr: [
    {
      dnsPtr: 'server.example.com',
      ip: '2001:db8::1',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  id: 42,
  ip: '131.232.99.1',
  labels: {
    'key0': 'labels0'
  },
  name: 'my-resource',
  protection: {
    mDelete: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  type: Type50.Ipv4,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



