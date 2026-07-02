# V2 Kubernetes Clusters Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetesCluster` | [`KubernetesCluster \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/kubernetes-cluster.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersResponse1 } from 'digitalocean-apilib';

const v2KubernetesClustersResponse1: V2KubernetesClustersResponse1 = {
  kubernetesCluster: {
    name: 'name8',
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
      },
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
    region: 'region4',
    version: 'version4',
    autoUpgrade: false,
    clusterSubnet: 'cluster_subnet0',
    createdAt: '2016-03-13T12:52:32.123Z',
    endpoint: 'endpoint6',
    ha: false,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



