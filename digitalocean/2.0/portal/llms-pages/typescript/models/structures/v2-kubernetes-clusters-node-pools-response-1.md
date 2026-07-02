# V2 Kubernetes Clusters Node Pools Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersNodePoolsResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nodePool` | [`NodePool \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/node-pool.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  State1,
  V2KubernetesClustersNodePoolsResponse1,
} from 'digitalocean-apilib';

const v2KubernetesClustersNodePoolsResponse1: V2KubernetesClustersNodePoolsResponse1 = {
  nodePool: {
    size: 's-1vcpu-2gb',
    count: 3,
    name: 'new-pool',
    autoScale: true,
    id: 'cdda885e-7663-40c8-bc74-3a036c66545d',
    labels: null,
    maxNodes: 6,
    minNodes: 3,
    nodes: [
      {
        createdAt: '2018-11-15T16:00:11Z',
        dropletId: ' ',
        id: '478247f8-b1bb-4f7a-8db9-2a5f8d4b8f8f',
        name: ' ',
        status: {
          state: State1.Provisioning,
        },
        updatedAt: '2018-11-15T16:00:11Z',
      },
      {
        createdAt: '2018-11-15T16:00:11Z',
        dropletId: ' ',
        id: 'ad12e744-c2a9-473d-8aa9-be5680500eb1',
        name: ' ',
        status: {
          state: State1.Provisioning,
        },
        updatedAt: '2018-11-15T16:00:11Z',
      },
      {
        createdAt: '2018-11-15T16:00:11Z',
        dropletId: ' ',
        id: 'e46e8d07-f58f-4ff1-9737-97246364400e',
        name: ' ',
        status: {
          state: State1.Provisioning,
        },
        updatedAt: '2018-11-15T16:00:11Z',
      }
    ],
    tags: [
      'production',
      'web-team',
      'front-end',
      'k8s',
      'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
      'k8s:worker'
    ],
    taints: [],
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



