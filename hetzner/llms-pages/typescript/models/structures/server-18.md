# Server 18

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcjE4


# Interface Name

`Server18`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backupWindow` | `string \| null` | Required | Time window (UTC) in which the backup will run, or null if the backups are not enabled |
| `created` | `string` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `datacenter` | [`Datacenter6`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/datacenter-6.md) | Required | Datacenter this Resource is located at |
| `id` | `number` | Required | ID of the Resource |
| `image` | [`Image \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/image.md) | Required | - |
| `includedTraffic` | `number \| null` | Required | Free Traffic for the current billing period in bytes |
| `ingoingTraffic` | `number \| null` | Required | Inbound Traffic for the current billing period in bytes |
| `iso` | [`Iso2 \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/iso-2.md) | Required | ISO Image that is attached to this Server. Null if no ISO is attached. |
| `labels` | `Record<string, string>` | Required | User-defined labels (key-value pairs) |
| `loadBalancers` | `number[] \| undefined` | Optional | - |
| `locked` | `boolean` | Required | True if Server has been locked and is not available to user |
| `name` | `string` | Required | Name of the Server (must be unique per Project and a valid hostname as per RFC 1123) |
| `outgoingTraffic` | `number \| null` | Required | Outbound Traffic for the current billing period in bytes |
| `placementGroup` | [`PlacementGroupNullable \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/placement-group-nullable.md) | Optional | - |
| `primaryDiskSize` | `number` | Required | Size of the primary Disk |
| `privateNet` | [`PrivateNet4[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/private-net-4.md) | Required | Private networks information |
| `protection` | [`Protection20`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/protection-20.md) | Required | Protection configuration for the Server |
| `publicNet` | [`PublicNet4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/public-net-4.md) | Required | Public network information. The Server's IPv4 address can be found in `public_net->ipv4->ip` |
| `rescueEnabled` | `boolean` | Required | True if rescue mode is enabled. Server will then boot into rescue system on next reboot |
| `serverType` | [`ServerType1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/server-type-1.md) | Required | Type of Server - determines how much ram, disk and cpu a Server has |
| `status` | [`Status73Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/status-73.md) | Required | Status of the Server |
| `volumes` | `number[] \| undefined` | Optional | IDs of Volumes assigned to this Server |


# Example

```ts
import {
  CpuTypeEnum,
  OsFlavorEnum,
  Server18,
  Status24Enum,
  Status72Enum,
  Status73Enum,
  StorageTypeEnum,
  Type22Enum,
  Type26Enum,
} from 'hetzner-cloud-apilib';

const server18: Server18 = {
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
    'key0': 'labels4',
    'key1': 'labels3',
    'key2': 'labels2'
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
  status: Status73Enum.Running,
  loadBalancers: [
    248
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
    199,
    200,
    201
  ],
};
```



