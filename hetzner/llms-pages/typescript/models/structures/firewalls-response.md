# Firewalls Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkZpcmV3YWxsc1Jlc3BvbnNl


# Interface Name

`FirewallsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `firewalls` | [`Firewall[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/firewall.md) | Required | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/meta.md) | Optional | - |


# Example

```ts
import {
  DirectionEnum,
  FirewallsResponse,
  ProtocolEnum,
  Type5Enum,
  Type6Enum,
} from 'hetzner-cloud-apilib';

const firewallsResponse: FirewallsResponse = {
  firewalls: [
    {
      appliedTo: [
        {
          type: Type6Enum.Server,
          appliedToResources: [
            {
              server: {
                id: 14,
              },
              type: Type5Enum.Server,
            }
          ],
          labelSelector: {
            selector: 'selector8',
          },
          server: {
            id: 14,
          },
        }
      ],
      created: '2016-01-30T23:55:00+00:00',
      id: 42,
      name: 'my-resource',
      rules: [
        {
          direction: DirectionEnum.In,
          protocol: ProtocolEnum.Udp,
          description: 'description2',
          destinationIps: [
            '28.239.13.1/32',
            '28.239.14.0/24',
            'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
          ],
          port: '80',
          sourceIps: [
            '28.239.13.1/32',
            '28.239.14.0/24',
            'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
          ],
        }
      ],
      labels: {
        'key0': 'labels4',
        'key1': 'labels5'
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
    },
  },
};
```



