# Create Server Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlc3BvbnNl

*This model accepts additional fields of type unknown.*


# Interface Name

`CreateServerResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `nextActions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `rootPassword` | `string \| null` | Required | Root password when no SSH keys have been specified |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-18.md) | Required | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CpuType,
  CreateServerResponse,
  OsFlavor,
  Status,
  Status24,
  Status72,
  Status73,
  StorageType,
  Type22,
  Type26,
} from 'hetzner-cloud-apilib';

const createServerResponse: CreateServerResponse = {
  action: {
    command: 'start_server',
    error: {
      code: 'action_failed',
      message: 'Action failed',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    finished: '2016-01-30T23:55:00+00:00',
    id: 42,
    progress: 100,
    resources: [
      {
        id: 42,
        type: 'server',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    started: '2016-01-30T23:55:00+00:00',
    status: Status.Running,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  nextActions: [
    {
      command: 'start_server',
      error: {
        code: 'action_failed',
        message: 'Action failed',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      finished: '2016-01-30T23:55:00+00:00',
      id: 42,
      progress: 100,
      resources: [
        {
          id: 42,
          type: 'server',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      started: '2016-01-30T23:55:00+00:00',
      status: Status.Success,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  rootPassword: 'YItygq1v3GYjjMomLaKc',
  server: {
    backupWindow: '22-02',
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
    id: 42,
    image: {
      boundTo: null,
      created: '2016-01-30T23:55:00+00:00',
      createdFrom: {
        id: 1,
        name: 'Server',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      deleted: null,
      deprecated: '2018-02-28T00:00:00+00:00',
      description: 'Ubuntu 20.04 Standard 64 bit',
      diskSize: 10,
      id: 42,
      imageSize: 2.3,
      labels: {
        'key0': 'labels4'
      },
      name: 'ubuntu-20.04',
      osFlavor: OsFlavor.Ubuntu,
      osVersion: '20.04',
      protection: {
        mDelete: false,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      status: Status24.Unavailable,
      type: Type22.Snapshot,
      rapidDeploy: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    includedTraffic: 654321,
    ingoingTraffic: 123456,
    iso: {
      deprecated: '2018-02-28T00:00:00+00:00',
      description: 'FreeBSD 11.0 x64',
      id: 42,
      name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
      type: Type26.Public,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    labels: {
      'key0': 'labels0',
      'key1': 'labels9'
    },
    locked: false,
    name: 'my-resource',
    outgoingTraffic: 123456,
    primaryDiskSize: 50,
    privateNet: [
      {
        aliasIps: [
          'alias_ips4'
        ],
        ip: '10.0.0.2',
        macAddress: '86:00:ff:2a:7d:e1',
        network: 4711,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    protection: {
      mDelete: false,
      rebuild: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    publicNet: {
      floatingIps: [
        478
      ],
      ipv4: {
        blocked: false,
        dnsPtr: 'server01.example.com',
        ip: '1.2.3.4',
        id: 42,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      ipv6: {
        blocked: false,
        dnsPtr: [
          {
            dnsPtr: 'server.example.com',
            ip: '2001:db8::1',
            additionalProperties: {
              'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
            },
          }
        ],
        ip: '2001:db8::/64',
        id: 42,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      firewalls: [
        {
          id: 250,
          status: Status72.Applied,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        {
          id: 250,
          status: Status72.Applied,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        }
      ],
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    rescueEnabled: false,
    serverType: {
      cores: 1,
      cpuType: CpuType.Shared,
      deprecated: false,
      description: 'CX11',
      disk: 25,
      id: 1,
      memory: 1,
      name: 'cx11',
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
      storageType: StorageType.Local,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    status: Status73.Starting,
    loadBalancers: [
      144,
      143,
      142
    ],
    placementGroup: {
      created: 'created8',
      id: 236,
      labels: {
        'key0': 'labels4'
      },
      name: 'name8',
      servers: [
        251,
        252,
        253
      ],
      type: 'type2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    volumes: [
      91,
      92
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



