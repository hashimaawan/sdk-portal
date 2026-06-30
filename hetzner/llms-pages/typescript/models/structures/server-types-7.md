# Server Types 7

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/typescript/x-redirect/JTI0bSUyRlNlcnZlclR5cGVzNw


# Interface Name

`ServerTypes7`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cores` | `number` | Required | Number of cpu cores a Server of this type will have |
| `cpuType` | [`CpuTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/cpu-type.md) | Required | Type of cpu |
| `deprecated` | `boolean` | Required | True if Server type is deprecated |
| `description` | `string` | Required | Description of the Server type |
| `disk` | `number` | Required | Disk size a Server of this type will have in GB |
| `id` | `number` | Required | ID of the Server type |
| `memory` | `number` | Required | Memory a Server of this type will have in GB |
| `name` | `string` | Required | Unique identifier of the Server type |
| `prices` | [`Price9[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/structures/price-9.md) | Required | Prices in different Locations |
| `storageType` | [`StorageTypeEnum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/typescript/models/enumerations/storage-type.md) | Required | Type of Server boot drive. Local has higher speed. Network has better availability. |


# Example

```ts
import {
  CpuTypeEnum,
  ServerTypes7,
  StorageTypeEnum,
} from 'hetzner-cloud-apilib';

const serverTypes7: ServerTypes7 = {
  cores: 1,
  cpuType: CpuTypeEnum.Shared,
  deprecated: false,
  description: 'CX11',
  disk: 24,
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



