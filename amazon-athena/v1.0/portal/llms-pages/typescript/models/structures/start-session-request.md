# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q


# Interface Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engineConfiguration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-configuration-1.md) | Required | - |
| `notebookVersion` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `sessionIdleTimeoutInMinutes` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 480` |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |


# Example

```ts
import { StartSessionRequest } from 'amazon-athenalib';

const startSessionRequest: StartSessionRequest = {
  workGroup: 'WorkGroup2',
  engineConfiguration: {
    maxConcurrentDpus: 94,
    coordinatorDpuSize: 1,
    defaultExecutorDpuSize: 1,
    additionalConfigs: {},
  },
  description: 'Description4',
  notebookVersion: 'NotebookVersion4',
  sessionIdleTimeoutInMinutes: 172,
  clientRequestToken: 'ClientRequestToken4',
};
```



