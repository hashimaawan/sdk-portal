# Node Pool

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRk5vZGVQb29s

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`NodePool`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `size` | `string` | Required | The slug identifier for the type of Droplet used as workers in the node pool. |
| `autoScale` | `boolean \| undefined` | Optional | A boolean value indicating whether auto-scaling is enabled for this node pool. |
| `count` | `number` | Required | The number of Droplet instances in the node pool. |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a specific node pool. |
| `labels` | [`unknown \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | An object containing a set of Kubernetes labels. The keys and are values are both user-defined. |
| `maxNodes` | `number \| undefined` | Optional | The maximum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `minNodes` | `number \| undefined` | Optional | The minimum number of nodes that this node pool can be auto-scaled to. The value will be `0` if `auto_scale` is set to `false`. |
| `name` | `string` | Required | A human-readable name for the node pool. |
| `nodes` | [`Node[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/node.md) | Optional, Read-only | An object specifying the details of a specific worker node in a node pool. |
| `tags` | `string[] \| undefined` | Optional | An array containing the tags applied to the node pool. All node pools are automatically tagged `k8s`, `k8s-worker`, and `k8s:$K8S_CLUSTER_ID`. |
| `taints` | [`Taint[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/taint.md) | Optional | An array of taints to apply to all nodes in a pool. Taints will automatically be applied to all existing nodes and any subsequent nodes added to the pool. When a taint is removed, it is removed from all nodes in the pool. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { NodePool } from 'digitalocean-apilib';

const nodePool: NodePool = {
  size: 's-1vcpu-2gb',
  count: 3,
  name: 'frontend-pool',
  autoScale: true,
  id: 'cdda885e-7663-40c8-bc74-3a036c66545d',
  labels: { 'key1': 'val1', 'key2': 'val2' },
  maxNodes: 6,
  minNodes: 3,
  tags: [
    'k8s',
    'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
    'k8s-worker',
    'production',
    'web-team'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



