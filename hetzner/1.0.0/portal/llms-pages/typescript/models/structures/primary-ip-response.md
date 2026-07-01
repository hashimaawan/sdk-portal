# Primary IP Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlByaW1hcnlJUFJlc3BvbnNl


# Interface Name

`PrimaryIPResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `primaryIp` | [`PrimaryIP1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/primary-ip-1.md) | Required | - |


# Example

```ts
import { PrimaryIPResponse, Type50Enum } from 'hetzner-cloud-apilib';

const primaryIPResponse: PrimaryIPResponse = {
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
      },
    },
    dnsPtr: [
      {
        dnsPtr: 'server.example.com',
        ip: '2001:db8::1',
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
    },
    type: Type50Enum.Ipv4,
  },
};
```



