# Get Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFNlc3Npb25SZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`GetSessionResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engineVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `engineConfiguration` | [`EngineConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-configuration-1.md) | Optional | - |
| `notebookVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `sessionConfiguration` | [`SessionConfiguration2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/session-configuration-2.md) | Optional | - |
| `status` | [`Status3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-3.md) | Optional | - |
| `statistics` | [`Statistics3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/statistics-3.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { GetSessionResponse } from 'amazon-athenalib';

const getSessionResponse: GetSessionResponse = {
  sessionId: 'SessionId6',
  description: 'Description4',
  workGroup: 'WorkGroup4',
  engineVersion: 'EngineVersion8',
  engineConfiguration: {
    maxConcurrentDpus: 94,
    coordinatorDpuSize: 1,
    defaultExecutorDpuSize: 1,
    additionalConfigs: {
      additionalProperties: {
        'exampleAdditionalProperty': 'AdditionalConfigs_additionalProperties5'
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



