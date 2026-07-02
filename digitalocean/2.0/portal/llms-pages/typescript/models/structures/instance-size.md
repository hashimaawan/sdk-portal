# Instance Size

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkluc3RhbmNlU2l6ZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`InstanceSize`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cpuType` | [`MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/enumerations/shared-shared-v-cpu-cores-dedicated-dedicated-v-cpu-cores.md) | Optional | **Default**: `MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Unspecified` |
| `cpus` | `string \| undefined` | Optional | - |
| `memoryBytes` | `string \| undefined` | Optional | - |
| `name` | `string \| undefined` | Optional | - |
| `slug` | `string \| undefined` | Optional | - |
| `tierDowngradeTo` | `string \| undefined` | Optional | - |
| `tierSlug` | `string \| undefined` | Optional | - |
| `tierUpgradeTo` | `string \| undefined` | Optional | - |
| `usdPerMonth` | `string \| undefined` | Optional | - |
| `usdPerSecond` | `string \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  InstanceSize,
  MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores,
} from 'digitalocean-apilib';

const instanceSize: InstanceSize = {
  cpuType: MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Shared,
  cpus: '3',
  memoryBytes: '1048',
  name: 'name',
  slug: 'basic',
  tierDowngradeTo: 'basic',
  tierSlug: 'basic',
  tierUpgradeTo: 'basic',
  usdPerMonth: '23',
  usdPerSecond: '0.00000001232',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



