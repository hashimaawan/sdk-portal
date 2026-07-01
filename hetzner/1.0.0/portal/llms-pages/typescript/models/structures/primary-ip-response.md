# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`PrimaryIpResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `primaryIp` | [`PrimaryIp1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/primary-ip-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PrimaryIpResponse, Type50 } from 'hetzner-cloud-apilib';

const primaryIpResponse: PrimaryIpResponse = {
  primaryIp: {
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
      'key0': 'labels2',
      'key1': 'labels1'
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
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



