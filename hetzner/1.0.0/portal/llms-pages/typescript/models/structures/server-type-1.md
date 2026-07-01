# Server Type 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclR5cGUx

Type of Server - determines how much ram, disk and cpu a Server has


# Interface Name

`ServerType1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cores` | `number` | Required | Number of cpu cores a Server of this type will have |
| `cpuType` | [`CpuTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `deprecated` | `boolean` | Required | True if Server type is deprecated |
| `description` | `string` | Required | Description of the Server type |
| `disk` | `number` | Required | Disk size a Server of this type will have in GB |
| `id` | `number` | Required | ID of the Server type |
| `memory` | `number` | Required | Memory a Server of this type will have in GB |
| `name` | `string` | Required | Unique identifier of the Server type |
| `prices` | [`Price9[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/structures/price-9.md) | Required | Prices in different Locations |
| `storageType` | [`StorageTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/typescript/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |


# Example

```ts
import {
  CpuTypeEnum,
  ServerType1,
  StorageTypeEnum,
} from 'hetzner-cloud-apilib';

const serverType1: ServerType1 = {
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
};
```



