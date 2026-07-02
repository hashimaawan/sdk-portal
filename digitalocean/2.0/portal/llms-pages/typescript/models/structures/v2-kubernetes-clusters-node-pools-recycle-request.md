# V2 Kubernetes Clusters Node Pools Recycle Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwTm9kZSUyNTIwUG9vbHMlMjUyMFJlY3ljbGUlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersNodePoolsRecycleRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nodes` | `string[] \| undefined` | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  V2KubernetesClustersNodePoolsRecycleRequest,
} from 'digitalocean-apilib';

const v2KubernetesClustersNodePoolsRecycleRequest: V2KubernetesClustersNodePoolsRecycleRequest = {
  nodes: [
    'd8db5e1a-6103-43b5-a7b3-8a948210a9fc'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



