# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg


# Interface Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/algorithm.md) | Required | Algorithm of the Load Balancer |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `number` | Required | ID of the Resource |
| `includedTraffic` | `number` | Required | Free Traffic for the current billing period in bytes |
| `ingoingTraffic` | `number \| null` | Required | Inbound Traffic for the current billing period in bytes |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `loadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-type.md) | Required | - |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/location.md) | Required | - |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `outgoingTraffic` | `number \| null` | Required | Outbound Traffic for the current billing period in bytes |
| `privateNet` | [`PrivateNet[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/private-net.md) | Required | Private networks information |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `publicNet` | [`PublicNet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/public-net.md) | Required | Public network information |
| `services` | [`LoadBalancerService[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-service.md) | Required | List of services that belong to this Load Balancer |
| `targets` | [`LoadBalancerTarget[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/load-balancer-target.md) | Required | List of targets that belong to this Load Balancer |


# Example

```ts
import {
  LoadBalancer,
  Protocol6Enum,
  Protocol7Enum,
  Status30Enum,
  Type28Enum,
  Type29Enum,
} from 'hetzner-cloud-apilib';

const loadBalancer: LoadBalancer = {
  algorithm: {
    type: Type28Enum.RoundRobin,
  },
  created: '2016-01-30T23:55:00+00:00',
  id: 42,
  includedTraffic: 10000,
  ingoingTraffic: 210,
  labels: {
    'key0': 'labels8',
    'key1': 'labels7'
  },
  loadBalancerType: {
    deprecated: '2016-01-30T23:50:00+00:00',
    description: 'LB11',
    id: 1,
    maxAssignedCertificates: 10,
    maxConnections: 20000,
    maxServices: 5,
    maxTargets: 25,
    name: 'lb11',
    prices: [
      {
        location: 'fsn1',
        priceHourly: {
          gross: '1.1900000000000000',
          net: '1.0000000000',
        },
        priceMonthly: {
          gross: '1.1900000000000000',
          net: '1.0000000000',
        },
      }
    ],
  },
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
  name: 'my-resource',
  outgoingTraffic: 36,
  privateNet: [
    {
      ip: '10.0.0.2',
      network: 4711,
    }
  ],
  protection: {
    mDelete: false,
  },
  publicNet: {
    enabled: false,
    ipv4: {
      dnsPtr: 'lb1.example.com',
      ip: '1.2.3.4',
    },
    ipv6: {
      dnsPtr: 'lb1.example.com',
      ip: '2001:db8::1',
    },
  },
  services: [
    {
      destinationPort: 80,
      healthCheck: {
        interval: 15,
        port: 4711,
        protocol: Protocol6Enum.Http,
        retries: 3,
        timeout: 10,
        http: {
          domain: 'domain4',
          path: 'path2',
          response: 'response8',
          statusCodes: [
            'status_codes0',
            'status_codes1',
            'status_codes2'
          ],
          tls: false,
        },
      },
      listenPort: 443,
      protocol: Protocol7Enum.Https,
      proxyprotocol: false,
      http: {
        certificates: [
          180
        ],
        cookieLifetime: 160,
        cookieName: 'cookie_name6',
        redirectHttp: false,
        stickySessions: false,
      },
    }
  ],
  targets: [
    {
      type: Type29Enum.Ip,
      healthStatus: [
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        },
        {
          listenPort: 142,
          status: Status30Enum.Unknown,
        }
      ],
      ip: {
        ip: 'ip8',
      },
      labelSelector: {
        selector: 'selector8',
      },
      server: {
        id: 14,
      },
      targets: [
        {
          healthStatus: [
            {
              listenPort: 142,
              status: Status30Enum.Unknown,
            },
            {
              listenPort: 142,
              status: Status30Enum.Unknown,
            }
          ],
          server: {
            id: 14,
          },
          type: 'type2',
          usePrivateIp: false,
        },
        {
          healthStatus: [
            {
              listenPort: 142,
              status: Status30Enum.Unknown,
            },
            {
              listenPort: 142,
              status: Status30Enum.Unknown,
            }
          ],
          server: {
            id: 14,
          },
          type: 'type2',
          usePrivateIp: false,
        },
        {
          healthStatus: [
            {
              listenPort: 142,
              status: Status30Enum.Unknown,
            },
            {
              listenPort: 142,
              status: Status30Enum.Unknown,
            }
          ],
          server: {
            id: 14,
          },
          type: 'type2',
          usePrivateIp: false,
        }
      ],
    }
  ],
};
```



