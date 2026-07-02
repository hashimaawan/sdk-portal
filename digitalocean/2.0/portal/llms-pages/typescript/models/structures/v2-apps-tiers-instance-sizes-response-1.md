# V2 Apps Tiers Instance Sizes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBUaWVycyUyNTIwSW5zdGFuY2UlMjUyMFNpemVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2AppsTiersInstanceSizesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `instanceSize` | [`InstanceSize \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/instance-size.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores,
  V2AppsTiersInstanceSizesResponse1,
} from 'digitalocean-apilib';

const v2AppsTiersInstanceSizesResponse1: V2AppsTiersInstanceSizesResponse1 = {
  instanceSize: {
    cpuType: MSharedSharedVcpuCoresDedicatedDedicatedVcpuCores.Dedicated,
    cpus: 'cpus4',
    memoryBytes: 'memory_bytes8',
    name: 'name8',
    slug: 'slug2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



