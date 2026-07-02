# V2 Kubernetes Clusters Destroy with Associated Resources Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBSZXNwb25zZQ

An object containing the IDs of resources associated with a Kubernetes cluster.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersDestroyWithAssociatedResourcesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancers` | [`LoadBalancer[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated load balancers that can be destroyed along with the cluster. |
| `volumeSnapshots` | [`LoadBalancer[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volume snapshots that can be destroyed along with the cluster. |
| `volumes` | [`LoadBalancer[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/load-balancer.md) | Optional | A list of names and IDs for associated volumes that can be destroyed along with the cluster. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  V2KubernetesClustersDestroyWithAssociatedResourcesResponse,
} from 'digitalocean-apilib';

const v2KubernetesClustersDestroyWithAssociatedResourcesResponse: V2KubernetesClustersDestroyWithAssociatedResourcesResponse = {
  loadBalancers: [
    {
      id: '4de7ac8b-495b-4884-9a69-1050c6793cd6',
      name: 'lb-001',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  volumeSnapshots: [
    {
      id: 'edb0478d-7436-11ea-86e6-0a58ac144b91',
      name: 'snapshot-001',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  volumes: [
    {
      id: 'ba49449a-7435-11ea-b89e-0a58ac14480f',
      name: 'volume-001',
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



