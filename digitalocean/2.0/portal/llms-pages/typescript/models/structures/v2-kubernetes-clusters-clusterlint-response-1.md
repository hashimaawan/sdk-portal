# V2 Kubernetes Clusters Clusterlint Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersClusterlintResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `runId` | `string \| undefined` | Optional | ID of the clusterlint run that can be used later to fetch the diagnostics. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import {
  V2KubernetesClustersClusterlintResponse1,
} from 'digitalocean-apilib';

const v2KubernetesClustersClusterlintResponse1: V2KubernetesClustersClusterlintResponse1 = {
  runId: '50c2f44c-011d-493e-aee5-361a4a0d1844',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



