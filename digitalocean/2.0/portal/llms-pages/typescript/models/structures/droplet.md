# Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkRyb3BsZXQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`Droplet`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `backupIds` | `number[]` | Required | An array of backup IDs of any backups that have been taken of the Droplet instance.  Droplet backups are enabled at the time of the instance creation. |
| `createdAt` | `string` | Required | A time value given in ISO8601 combined date and time format that represents when the Droplet was created. |
| `disk` | `number` | Required | The size of the Droplet's disk in gigabytes. |
| `features` | `string[]` | Required | An array of features enabled on this Droplet. |
| `id` | `number` | Required | A unique identifier for each Droplet instance. This is automatically generated upon Droplet creation. |
| `image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/image-1.md) | Required | - |
| `kernel` | [`Kernel \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/kernel.md) | Optional | **Note**: All Droplets created after March 2017 use internal kernels by default.<br>These Droplets will have this attribute set to `null`.<br><br>The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)<br>for Droplets with externally managed kernels. This will initially be set to<br>the kernel of the base image when the Droplet is created. |
| `locked` | `boolean` | Required | A boolean value indicating whether the Droplet has been locked, preventing actions by users. |
| `memory` | `number` | Required | Memory of the Droplet in megabytes.<br><br>**Constraints**: *Multiple Of*: `8` |
| `name` | `string` | Required | The human-readable name set for the Droplet instance. |
| `networks` | [`Networks`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/networks.md) | Required | The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is. |
| `nextBackupWindow` | [`NextBackupWindow \| null`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/next-backup-window.md) | Required | The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/region.md) | Required | - |
| `size` | [`Size`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/size.md) | Required | - |
| `sizeSlug` | `string` | Required | The unique slug identifier for the size of this Droplet. |
| `snapshotIds` | `number[]` | Required | An array of snapshot IDs of any snapshots created from the Droplet instance. |
| `status` | [`Status8`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/status-8.md) | Required | A status string indicating the state of the Droplet instance. This may be "new", "active", "off", or "archive". |
| `tags` | `string[]` | Required | An array of Tags the Droplet has been tagged with. |
| `vcpus` | `number` | Required | The number of virtual CPUs. |
| `volumeIds` | `string[]` | Required | A flat array including the unique identifier for each Block Storage volume attached to the Droplet. |
| `vpcUuid` | `string \| undefined` | Optional | A string specifying the UUID of the VPC to which the Droplet is assigned. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  Distribution,
  Droplet,
  Region2,
  Status7,
  Status8,
  Type10,
  Type11,
  Type9,
} from 'digitalocean-apilib';

const droplet: Droplet = {
  backupIds: [
    53893572
  ],
  createdAt: '2020-07-21T18:37:44Z',
  disk: 25,
  features: [
    'backups',
    'private_networking',
    'ipv6'
  ],
  id: 3164444,
  image: {
    createdAt: '2020-05-04T22:23:02Z',
    description: 'description6',
    distribution: Distribution.Ubuntu,
    errorMessage: 'error_message8',
    id: 7555620,
    minDiskSize: 20,
    name: 'Nifty New Snapshot',
    mPublic: true,
    regions: [
      Region2.Nyc1,
      Region2.Nyc2
    ],
    sizeGigabytes: 2.34,
    slug: 'nifty1',
    status: Status7.New,
    tags: [
      'base-image',
      'prod'
    ],
    type: Type9.Snapshot,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  locked: false,
  memory: 1024,
  name: 'example.com',
  networks: {
    v4: [
      {
        gateway: 'gateway2',
        ipAddress: 'ip_address2',
        netmask: 'netmask2',
        type: Type10.Public,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        gateway: 'gateway2',
        ipAddress: 'ip_address2',
        netmask: 'netmask2',
        type: Type10.Public,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        gateway: 'gateway2',
        ipAddress: 'ip_address2',
        netmask: 'netmask2',
        type: Type10.Public,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    v6: [
      {
        gateway: 'gateway4',
        ipAddress: 'ip_address4',
        netmask: 106,
        type: Type11.Public,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      {
        gateway: 'gateway4',
        ipAddress: 'ip_address4',
        netmask: 106,
        type: Type11.Public,
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      }
    ],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  nextBackupWindow: {
    end: '2019-12-04T23:00:00Z',
    start: '2019-12-04T00:00:00Z',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  region: {
    available: true,
    features: [
      'private_networking',
      'backups',
      'ipv6',
      'metadata',
      'install_agent',
      'storage',
      'image_transfer'
    ],
    name: 'New York 3',
    sizes: [
      's-1vcpu-1gb',
      's-1vcpu-2gb',
      's-1vcpu-3gb',
      's-2vcpu-2gb',
      's-3vcpu-1gb',
      's-2vcpu-4gb',
      's-4vcpu-8gb',
      's-6vcpu-16gb',
      's-8vcpu-32gb',
      's-12vcpu-48gb',
      's-16vcpu-64gb',
      's-20vcpu-96gb',
      's-24vcpu-128gb',
      's-32vcpu-192g'
    ],
    slug: 'nyc3',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  size: {
    available: true,
    description: 'Basic',
    disk: 25,
    memory: 1024,
    priceHourly: 0.00743999984115362,
    priceMonthly: 5,
    regions: [
      'ams2',
      'ams3',
      'blr1',
      'fra1',
      'lon1',
      'nyc1',
      'nyc2',
      'nyc3',
      'sfo1',
      'sfo2',
      'sfo3',
      'sgp1',
      'tor1'
    ],
    slug: 's-1vcpu-1gb',
    transfer: 1,
    vcpus: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  sizeSlug: 's-1vcpu-1gb',
  snapshotIds: [
    67512819
  ],
  status: Status8.Active,
  tags: [
    'web',
    'env:prod'
  ],
  vcpus: 1,
  volumeIds: [
    '506f78a4-e098-11e5-ad9f-000f53306ae1'
  ],
  kernel: {
    id: 16,
    name: 'name4',
    version: 'version0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  vpcUuid: '760e09ef-dc84-11e8-981e-3cfdfeaae000',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



