# V2 Kubernetes Clusters Clusterlint Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersClusterlintRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `excludeChecks` | `string[] \| undefined` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `excludeGroups` | `string[] \| undefined` | Optional | An array of check groups that will be omitted when clusterlint executes checks. |
| `includeChecks` | `string[] \| undefined` | Optional | An array of checks that will be run when clusterlint executes checks. |
| `includeGroups` | `string[] \| undefined` | Optional | An array of check groups that will be run when clusterlint executes checks. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersClusterlintRequest } from 'digitalocean-apilib';

const v2KubernetesClustersClusterlintRequest: V2KubernetesClustersClusterlintRequest = {
  excludeChecks: [
    'default-namespace'
  ],
  excludeGroups: [
    'workload-health'
  ],
  includeChecks: [
    'bare-pods',
    'resource-requirements'
  ],
  includeGroups: [
    'basic',
    'doks',
    'security'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



