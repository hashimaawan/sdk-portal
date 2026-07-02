# V2 Kubernetes Clusters User Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXNlciUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersUserResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetesClusterUser` | [`KubernetesClusterUser \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/kubernetes-cluster-user.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersUserResponse } from 'digitalocean-apilib';

const v2KubernetesClustersUserResponse: V2KubernetesClustersUserResponse = {
  kubernetesClusterUser: {
    groups: [
      'groups8'
    ],
    username: 'username6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



