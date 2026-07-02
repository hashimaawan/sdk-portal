# V2 Apps Tiers Instance Sizes Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsTiersInstanceSizesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `discountPercent` | `number \| undefined` | Optional | - |
| `instanceSizes` | [`InstanceSize[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/instance-size.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores,
  V2AppsTiersInstanceSizesResponse,
} from 'digitalocean-apilib';

const v2AppsTiersInstanceSizesResponse: V2AppsTiersInstanceSizesResponse = {
  discountPercent: 2.32,
  instanceSizes: [
    {
      cpuType: MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Dedicated,
      cpus: 'cpus4',
      memoryBytes: 'memory_bytes8',
      name: 'name8',
      slug: 'slug8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



