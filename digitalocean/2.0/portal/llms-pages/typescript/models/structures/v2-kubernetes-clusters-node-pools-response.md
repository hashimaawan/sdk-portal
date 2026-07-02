# V2 Kubernetes Clusters Node Pools Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersNodePoolsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nodePools` | [`NodePool[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/node-pool.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersNodePoolsResponse } from 'digitalocean-apilib';

const v2KubernetesClustersNodePoolsResponse: V2KubernetesClustersNodePoolsResponse = {
  nodePools: [
    {
      size: 'size6',
      count: 206,
      name: 'name4',
      autoScale: false,
      id: '000013be-0000-0000-0000-000000000000',
      labels: { 'key1': 'val1', 'key2': 'val2' },
      maxNodes: 118,
      minNodes: 54,
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



