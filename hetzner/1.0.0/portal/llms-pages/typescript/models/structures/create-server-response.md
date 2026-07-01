# Create Server Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRkNyZWF0ZVNlcnZlclJlc3BvbnNl


# Interface Name

`CreateServerResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `nextActions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/action.md) | Required | - |
| `rootPassword` | `string \| null` | Required | Root password when no SSH keys have been specified |
| `server` | [`Server18`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-18.md) | Required | - |


# Example

```ts
import {
  CpuTypeEnum,
  CreateServerResponse,
  OsFlavorEnum,
  Status24Enum,
  Status72Enum,
  Status73Enum,
  StatusEnum,
  StorageTypeEnum,
  Type22Enum,
  Type26Enum,
} from 'hetzner-cloud-apilib';

const createServerResponse: CreateServerResponse = {
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
  nextActions: [
    {
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
      status: StatusEnum.Success,
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
    id: 42,
    image: {
      boundTo: null,
      created: '2016-01-30T23:55:00+00:00',
      createdFrom: {
        id: 1,
        name: 'Server',
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
      osFlavor: OsFlavorEnum.Ubuntu,
      osVersion: '20.04',
      protection: {
        mDelete: false,
      },
      status: Status24Enum.Unavailable,
      type: Type22Enum.Snapshot,
      rapidDeploy: false,
    },
    includedTraffic: 654321,
    ingoingTraffic: 123456,
    iso: {
      deprecated: '2018-02-28T00:00:00+00:00',
      description: 'FreeBSD 11.0 x64',
      id: 42,
      name: 'FreeBSD-11.0-RELEASE-amd64-dvd1',
      type: Type26Enum.Public,
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
      }
    ],
    protection: {
      mDelete: false,
      rebuild: false,
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
      },
      ipv6: {
        blocked: false,
        dnsPtr: [
          {
            dnsPtr: 'server.example.com',
            ip: '2001:db8::1',
          }
        ],
        ip: '2001:db8::/64',
        id: 42,
      },
      firewalls: [
        {
          id: 250,
          status: Status72Enum.Applied,
        },
        {
          id: 250,
          status: Status72Enum.Applied,
        }
      ],
    },
    rescueEnabled: false,
    serverType: {
      cores: 1,
      cpuType: CpuTypeEnum.Shared,
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
          },
          priceMonthly: {
            gross: '1.1900000000000000',
            net: '1.0000000000',
          },
        }
      ],
      storageType: StorageTypeEnum.Local,
    },
    status: Status73Enum.Starting,
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
    },
    volumes: [
      91,
      92
    ],
  },
};
```



