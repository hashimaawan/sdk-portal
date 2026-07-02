# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.


# Interface Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `executorType` | [`ExecutorType2Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/executor-type-2.md) | Optional | - |
| `startDateTime` | `number \| undefined` | Optional | - |
| `terminationDateTime` | `number \| undefined` | Optional | - |
| `executorState` | [`ExecutorState3Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/executor-state-3.md) | Optional | - |
| `executorSize` | `number \| undefined` | Optional | - |


# Example

```ts
import {
  ExecutorState3Enum,
  ExecutorType2Enum,
  ExecutorsSummary,
} from 'amazon-athenalib';

const executorsSummary: ExecutorsSummary = {
  executorId: 'ExecutorId8',
  executorType: ExecutorType2Enum.WORKER,
  startDateTime: 52,
  terminationDateTime: 56,
  executorState: ExecutorState3Enum.CREATING,
  executorSize: 222,
};
```



