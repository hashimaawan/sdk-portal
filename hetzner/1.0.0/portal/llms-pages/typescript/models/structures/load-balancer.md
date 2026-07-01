# Load Balancer

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlcg

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancer`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `algorithm` | [`Algorithm`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/algorithm.md) | Required | Algorithm of the Load Balancer |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `id` | `number` | Required | ID of the Resource |
| `includedTraffic` | `number` | Required | Free Traffic for the current billing period in bytes |
| `ingoingTraffic` | `number \| null` | Required | Inbound Traffic for the current billing period in bytes |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `loadBalancerType` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-type.md) | Required | - |
| `location` | [`Location`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/location.md) | Required | - |
| `name` | `string` | Required | Name of the Resource. Must be unique per Project. |
| `outgoingTraffic` | `number \| null` | Required | Outbound Traffic for the current billing period in bytes |
| `privateNet` | [`PrivateNet[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/private-net.md) | Required | Private networks information |
| `protection` | [`Protection`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/protection.md) | Required | Protection configuration for the Resource |
| `publicNet` | [`PublicNet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/public-net.md) | Required | Public network information |
| `services` | [`LoadBalancerService[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-service.md) | Required | List of services that belong to this Load Balancer |
| `targets` | [`LoadBalancerTarget[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer-target.md) | Required | List of targets that belong to this Load Balancer |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  LoadBalancer,
  Protocol6,
  Protocol7,
  Status30,
  Type28,
  Type29,
} from 'hetzner-cloud-apilib';

const loadBalancer: LoadBalancer = {
  algorithm: {
    type: Type28.RoundRobin,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
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
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        priceMonthly: {
          gross: '1.1900000000000000',
          net: '1.0000000000',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
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
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  name: 'my-resource',
  outgoingTraffic: 36,
  privateNet: [
    {
      ip: '10.0.0.2',
      network: 4711,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  protection: {
    mDelete: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  publicNet: {
    enabled: false,
    ipv4: {
      dnsPtr: 'lb1.example.com',
      ip: '1.2.3.4',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    ipv6: {
      dnsPtr: 'lb1.example.com',
      ip: '2001:db8::1',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  services: [
    {
      destinationPort: 80,
      healthCheck: {
        interval: 15,
        port: 4711,
        protocol: Protocol6.Http,
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
      protocol: Protocol7.Https,
      proxyprotocol: false,
      http: {
        certificates: [
          180
        ],
        cookieLifetime: 160,
        cookieName: 'cookie_name6',
        redirectHttp: false,
        stickySessions: false,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  targets: [
    {
      type: Type29.Ip,
      healthStatus: [
        {
          listenPort: 142,
          status: Status30.Unknown,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          listenPort: 142,
          status: Status30.Unknown,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      ip: {
        ip: 'ip8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      labelSelector: {
        selector: 'selector8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      server: {
        id: 14,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      targets: [
        {
          healthStatus: [
            {
              listenPort: 142,
              status: Status30.Unknown,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            {
              listenPort: 142,
              status: Status30.Unknown,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            }
          ],
          server: {
            id: 14,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          type: 'type2',
          usePrivateIp: false,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          healthStatus: [
            {
              listenPort: 142,
              status: Status30.Unknown,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            {
              listenPort: 142,
              status: Status30.Unknown,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            }
          ],
          server: {
            id: 14,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          type: 'type2',
          usePrivateIp: false,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          healthStatus: [
            {
              listenPort: 142,
              status: Status30.Unknown,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            },
            {
              listenPort: 142,
              status: Status30.Unknown,
              additionalProperties: {
                'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
              },
            }
          ],
          server: {
            id: 14,
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          },
          type: 'type2',
          usePrivateIp: false,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



