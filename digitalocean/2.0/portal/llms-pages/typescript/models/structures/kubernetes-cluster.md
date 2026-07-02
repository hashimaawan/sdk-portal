# Kubernetes Cluster

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRkt1YmVybmV0ZXNDbHVzdGVy

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`KubernetesCluster`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoUpgrade` | `boolean \| undefined` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` |
| `clusterSubnet` | `string \| undefined` | Optional, Read-only | The range of IP addresses in the overlay network of the Kubernetes cluster in CIDR notation. |
| `createdAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was created. |
| `endpoint` | `string \| undefined` | Optional, Read-only | The base URL of the API server on the Kubernetes master node. |
| `ha` | `boolean \| undefined` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` |
| `id` | `string \| undefined` | Optional, Read-only | A unique ID that can be used to identify and reference a Kubernetes cluster. |
| `ipv4` | `string \| undefined` | Optional, Read-only | The public IPv4 address of the Kubernetes master node. This will not be set if high availability is configured on the cluster (v1.21+) |
| `maintenancePolicy` | [`MaintenancePolicy \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. |
| `name` | `string` | Required | A human-readable name for a Kubernetes cluster. |
| `nodePools` | [`NodePool[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/node-pool.md) | Required | An object specifying the details of the worker nodes available to the Kubernetes cluster. |
| `region` | `string` | Required | The slug identifier for the region where the Kubernetes cluster is located. |
| `registryEnabled` | `boolean \| undefined` | Optional, Read-only | A read-only boolean value indicating if a container registry is integrated with the cluster. |
| `serviceSubnet` | `string \| undefined` | Optional, Read-only | The range of assignable IP addresses for services running in the Kubernetes cluster in CIDR notation. |
| `status` | [`Status11 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/status-11.md) | Optional, Read-only | An object containing a `state` attribute whose value is set to a string indicating the current status of the cluster. |
| `surgeUpgrade` | `boolean \| undefined` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` |
| `tags` | `string[] \| undefined` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. |
| `updatedAt` | `string \| undefined` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the Kubernetes cluster was last updated. |
| `version` | `string` | Required | The slug identifier for the version of Kubernetes used for the cluster. If set to a minor version (e.g. "1.14"), the latest version within it will be used (e.g. "1.14.6-do.1"); if set to "latest", the latest published version will be used. See the `/v2/kubernetes/options` endpoint to find all currently available versions. |
| `vpcUuid` | `string \| undefined` | Optional | A string specifying the UUID of the VPC to which the Kubernetes cluster is assigned. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { KubernetesCluster } from 'digitalocean-apilib';

const kubernetesCluster: KubernetesCluster = {
  name: 'prod-cluster-01',
  nodePools: [
    {
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
    }
  ],
  region: 'nyc1',
  version: '1.18.6-do.0',
  autoUpgrade: true,
  clusterSubnet: '10.244.0.0/16',
  createdAt: '2018-11-15T16:00:11Z',
  endpoint: 'https://bd5f5959-5e1e-4205-a714-a914373942af.k8s.ondigitalocean.com',
  ha: true,
  id: 'bd5f5959-5e1e-4205-a714-a914373942af',
  ipv4: '68.183.121.157',
  registryEnabled: true,
  serviceSubnet: '10.245.0.0/16',
  surgeUpgrade: true,
  tags: [
    'k8s',
    'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
    'production',
    'web-team'
  ],
  updatedAt: '2018-11-15T16:00:11Z',
  vpcUuid: 'c33931f2-a26a-4e61-b85c-4e95a2ec431b',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



