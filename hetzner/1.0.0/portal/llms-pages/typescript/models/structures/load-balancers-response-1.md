# Load Balancers Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VycyUyNTIwUmVzcG9uc2Ux


# Interface Name

`LoadBalancersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `loadBalancer` | [`LoadBalancer`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/load-balancer.md) | Required | - |


# Example

```ts
import {
  LoadBalancersResponse1,
  Protocol6Enum,
  Protocol7Enum,
  Status30Enum,
  StatusEnum,
  Type28Enum,
  Type29Enum,
} from 'hetzner-cloud-apilib';

const loadBalancersResponse1: LoadBalancersResponse1 = {
  action: {
    command: 'start_server',
    error: {
      code: 'action_failed',
      message: 'Action failed',
    },
    finished: '2016-01-30T23:55:00+00:00',
    id: 42,
    progress: 100,
    resources: [
      {
        id: 42,
        type: 'server',
      }
    ],
    started: '2016-01-30T23:55:00+00:00',
    status: StatusEnum.Running,
  },
  loadBalancer: {
    algorithm: {
      type: Type28Enum.RoundRobin,
    },
    created: '2016-01-30T23:55:00+00:00',
    id: 42,
    includedTraffic: 10000,
    ingoingTraffic: 216,
    labels: {
      'key0': 'labels2',
      'key1': 'labels1'
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
    outgoingTraffic: 42,
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
  },
};
```



