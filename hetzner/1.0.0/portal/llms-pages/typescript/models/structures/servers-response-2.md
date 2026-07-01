# Servers Response 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMFJlc3BvbnNlMg


# Interface Name

`ServersResponse2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `server` | [`Server18 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/server-18.md) | Optional | - |


# Example

```ts
import {
  CpuTypeEnum,
  OsFlavorEnum,
  ServersResponse2,
  Status24Enum,
  Status72Enum,
  Status73Enum,
  StorageTypeEnum,
  Type22Enum,
  Type26Enum,
} from 'hetzner-cloud-apilib';

const serversResponse2: ServersResponse2 = {
  server: {
    backupWindow: 'backup_window2',
    created: 'created4',
    datacenter: {
      description: 'description0',
      id: 200,
      location: {
        city: 'city6',
        country: 'country8',
        description: 'description6',
        id: 187.14,
        latitude: 194.62,
        longitude: 59.18,
        name: 'name4',
        networkZone: 'network_zone2',
      },
      name: 'name0',
      serverTypes: {
        available: [
          23.74
        ],
        availableForMigration: [
          201.65,
          201.66
        ],
        supported: [
          69.52,
          69.53,
          69.54
        ],
      },
    },
    id: 14,
    image: {
      boundTo: 186,
      created: 'created6',
      createdFrom: {
        id: 60,
        name: 'name6',
      },
      deleted: 'deleted4',
      deprecated: 'deprecated8',
      description: 'description6',
      diskSize: 244.18,
      id: 128,
      imageSize: 141.34,
      labels: {
        'key0': 'labels4'
      },
      name: 'name6',
      osFlavor: OsFlavorEnum.Debian,
      osVersion: 'os_version4',
      protection: {
        mDelete: false,
      },
      status: Status24Enum.Unavailable,
      type: Type22Enum.App,
      rapidDeploy: false,
    },
    includedTraffic: 123.68,
    ingoingTraffic: 151.82,
    iso: {
      deprecated: 'deprecated0',
      description: 'description2',
      id: 66,
      name: 'name8',
      type: Type26Enum.Public,
    },
    labels: {
      'key0': 'labels0',
      'key1': 'labels9'
    },
    locked: false,
    name: 'name4',
    outgoingTraffic: 129.6,
    primaryDiskSize: 19.88,
    privateNet: [
      {
        aliasIps: [
          'alias_ips4'
        ],
        ip: 'ip6',
        macAddress: 'mac_address0',
        network: 154,
      },
      {
        aliasIps: [
          'alias_ips4'
        ],
        ip: 'ip6',
        macAddress: 'mac_address0',
        network: 154,
      }
    ],
    protection: {
      mDelete: false,
      rebuild: false,
    },
    publicNet: {
      floatingIps: [
        54,
        55,
        56
      ],
      ipv4: {
        blocked: false,
        dnsPtr: 'dns_ptr4',
        ip: 'ip2',
        id: 104,
      },
      ipv6: {
        blocked: false,
        dnsPtr: [
          {
            dnsPtr: 'dns_ptr0',
            ip: 'ip6',
          },
          {
            dnsPtr: 'dns_ptr0',
            ip: 'ip6',
          }
        ],
        ip: 'ip0',
        id: 8,
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
      cores: 12.84,
      cpuType: CpuTypeEnum.Shared,
      deprecated: false,
      description: 'description0',
      disk: 14.32,
      id: 30,
      memory: 21.2,
      name: 'name0',
      prices: [
        {
          location: 'location8',
          priceHourly: {
            gross: 'gross4',
            net: 'net2',
          },
          priceMonthly: {
            gross: 'gross2',
            net: 'net0',
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



