# V2 Kubernetes Clusters Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `autoUpgrade` | `boolean \| undefined` | Optional | A boolean value indicating whether the cluster will be automatically upgraded to new patch releases during its maintenance window.<br><br>**Default**: `false` |
| `ha` | `boolean \| undefined` | Optional | A boolean value indicating whether the control plane is run in a highly available configuration in the cluster. Highly available control planes incur less downtime. The property cannot be disabled.<br><br>**Default**: `false` |
| `maintenancePolicy` | [`MaintenancePolicy \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/maintenance-policy.md) | Optional | An object specifying the maintenance window policy for the Kubernetes cluster. |
| `name` | `string` | Required | A human-readable name for a Kubernetes cluster. |
| `surgeUpgrade` | `boolean \| undefined` | Optional | A boolean value indicating whether surge upgrade is enabled/disabled for the cluster. Surge upgrade makes cluster upgrades fast and reliable by bringing up new nodes before destroying the outdated nodes.<br><br>**Default**: `false` |
| `tags` | `string[] \| undefined` | Optional | An array of tags applied to the Kubernetes cluster. All clusters are automatically tagged `k8s` and `k8s:$K8S_CLUSTER_ID`. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { Day, V2KubernetesClustersRequest } from 'digitalocean-apilib';

const v2KubernetesClustersRequest: V2KubernetesClustersRequest = {
  name: 'prod-cluster-01',
  autoUpgrade: true,
  ha: true,
  maintenancePolicy: {
    day: Day.Any,
    duration: 'duration4',
    startTime: 'start_time2',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  surgeUpgrade: true,
  tags: [
    'k8s',
    'k8s:bd5f5959-5e1e-4205-a714-a914373942af',
    'production',
    'web-team'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



