# V2 Kubernetes Clusters Destroy with Associated Resources Selective Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwRGVzdHJveSUyNTIwV2l0aCUyNTIwQXNzb2NpYXRlZCUyNTIwUmVzb3VyY2VzJTI1MjBTZWxlY3RpdmUlMjUyMFJlcXVlc3Q

An object containing the IDs of resources to be destroyed along with their associated with a Kubernetes cluster.

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `loadBalancers` | `string[] \| undefined` | Optional | A list of IDs for associated load balancers to destroy along with the cluster. |
| `volumeSnapshots` | `string[] \| undefined` | Optional | A list of IDs for associated volume snapshots to destroy along with the cluster. |
| `volumes` | `string[] \| undefined` | Optional | A list of IDs for associated volumes to destroy along with the cluster. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest,
} from 'digitalocean-apilib';

const v2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest: V2KubernetesClustersDestroyWithAssociatedResourcesSelectiveRequest = {
  loadBalancers: [
    '4de7ac8b-495b-4884-9a69-1050c6793cd6'
  ],
  volumeSnapshots: [
    'edb0478d-7436-11ea-86e6-0a58ac144b91'
  ],
  volumes: [
    'ba49449a-7435-11ea-b89e-0a58ac14480f'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



