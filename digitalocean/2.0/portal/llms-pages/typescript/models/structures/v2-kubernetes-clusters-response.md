# V2 Kubernetes Clusters Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kubernetesClusters` | [`KubernetesCluster[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/kubernetes-cluster.md) | Optional | - |
| `links` | [`Links \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/links.md) | Optional | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/meta.md) | Required | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersResponse } from 'digitalocean-apilib';

const v2KubernetesClustersResponse: V2KubernetesClustersResponse = {
  meta: {
    total: 1,
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  kubernetesClusters: [
    {
      name: 'name2',
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
      region: 'region8',
      version: 'version8',
      autoUpgrade: false,
      clusterSubnet: 'cluster_subnet4',
      createdAt: '2016-03-13T12:52:32.123Z',
      endpoint: 'endpoint0',
      ha: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'name2',
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
      region: 'region8',
      version: 'version8',
      autoUpgrade: false,
      clusterSubnet: 'cluster_subnet4',
      createdAt: '2016-03-13T12:52:32.123Z',
      endpoint: 'endpoint0',
      ha: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      name: 'name2',
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
      region: 'region8',
      version: 'version8',
      autoUpgrade: false,
      clusterSubnet: 'cluster_subnet4',
      createdAt: '2016-03-13T12:52:32.123Z',
      endpoint: 'endpoint0',
      ha: false,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  links: {
    pages: {
      last: 'last6',
      next: 'next2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



