# Load Balancers Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`LoadBalancersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancers` | [`LoadBalancer[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer.md) | Required | - |
| `meta` | [`Meta \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/meta.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  LoadBalancersResponse,
  Protocol6,
  Protocol7,
  Status30,
  Type28,
  Type29,
} from 'hetzner-cloud-apilib';

const loadBalancersResponse: LoadBalancersResponse = {
  loadBalancers: [
    {
      algorithm: {
        type: Type28.RoundRobin,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      created: '2016-01-30T23:55:00+00:00',
      id: 42,
      includedTraffic: 10000,
      ingoingTraffic: 204,
      labels: {
        'key0': 'labels8',
        'key1': 'labels7',
        'key2': 'labels6'
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
      outgoingTraffic: 30,
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



