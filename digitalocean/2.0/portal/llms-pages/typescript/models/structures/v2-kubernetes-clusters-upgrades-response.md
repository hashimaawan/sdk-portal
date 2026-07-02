# V2 Kubernetes Clusters Upgrades Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwVXBncmFkZXMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersUpgradesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `availableUpgradeVersions` | [`AvailableUpgradeVersion[] \| null \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/available-upgrade-version.md) | Optional | - |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersUpgradesResponse } from 'digitalocean-apilib';

const v2KubernetesClustersUpgradesResponse: V2KubernetesClustersUpgradesResponse = {
  availableUpgradeVersions: [
    {
      kubernetesVersion: 'kubernetes_version0',
      slug: 'slug2',
      supportedFeatures: [
        'supported_features3'
      ],
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



