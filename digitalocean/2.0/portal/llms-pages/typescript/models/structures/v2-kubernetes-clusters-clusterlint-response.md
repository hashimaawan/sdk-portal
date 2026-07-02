# V2 Kubernetes Clusters Clusterlint Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/typescript/x-redirect/JTI0bSUyRlYyJTI1MjBLdWJlcm5ldGVzJTI1MjBDbHVzdGVycyUyNTIwQ2x1c3RlcmxpbnQlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [unknown](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md).*


# Interface Name

`V2KubernetesClustersClusterlintResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `completedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was completed. |
| `diagnostics` | [`Diagnostic[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/diagnostic.md) | Optional | An array of diagnostics reporting potential problems for the given cluster. |
| `requestedAt` | `string \| undefined` | Optional | A time value given in ISO8601 combined date and time format that represents when the schedule clusterlint run request was made. |
| `runId` | `string \| undefined` | Optional | Id of the clusterlint run that can be used later to fetch the diagnostics. |
| `additionalProperties` | [`Record<string, unknown>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/typescript/models/structures/object.md) | Optional | - |


# Example

```ts
import { V2KubernetesClustersClusterlintResponse } from 'digitalocean-apilib';

const v2KubernetesClustersClusterlintResponse: V2KubernetesClustersClusterlintResponse = {
  completedAt: '2019-10-30T05:34:11Z',
  diagnostics: [
    {
      checkName: 'check_name8',
      message: 'message2',
      object: {
        kind: 'kind0',
        name: 'name2',
        namespace: 'namespace0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      severity: 'severity2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      checkName: 'check_name8',
      message: 'message2',
      object: {
        kind: 'kind0',
        name: 'name2',
        namespace: 'namespace0',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      severity: 'severity2',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  requestedAt: '2019-10-30T05:34:07Z',
  runId: '50c2f44c-011d-493e-aee5-361a4a0d1844',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



