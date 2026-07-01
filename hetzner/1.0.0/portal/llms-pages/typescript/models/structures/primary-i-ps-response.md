# Primary I Ps Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaW1hcnlJUHNSZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`PrimaryIPsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `primaryIps` | [`PrimaryIp1[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/primary-ip-1.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { PrimaryIPsResponse, Type50 } from 'hetzner-cloud-apilib';

const primaryIPsResponse: PrimaryIPsResponse = {
  primaryIps: [
    {
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
        'key1': 'labels3',
        'key2': 'labels4'
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
    }
  ],
  meta: {
    pagination: {
      lastPage: 77.7,
      nextPage: 209.18,
      page: 17.58,
      perPage: 13.34,
      previousPage: 50.02,
      totalEntries: 206.64,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



