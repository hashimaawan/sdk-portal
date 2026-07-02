# Executors Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkV4ZWN1dG9yc1N1bW1hcnk

Contains summary information about an executor.

*This model accepts additional fields of type unknown.*


# Interface Name

`ExecutorsSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executorId` | `string` | Required | **Constraints**: *Maximum Length*: `100000`, *Pattern*: `.*` |
| `executorType` | [`ExecutorType2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/executor-type-2.md) | Optional | - |
| `startDateTime` | `number \| undefined` | Optional | - |
| `terminationDateTime` | `number \| undefined` | Optional | - |
| `executorState` | [`ExecutorState3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/executor-state-3.md) | Optional | - |
| `executorSize` | `number \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ExecutorState3,
  ExecutorType2,
  ExecutorsSummary,
} from 'amazon-athenalib';

const executorsSummary: ExecutorsSummary = {
  executorId: 'ExecutorId8',
  executorType: ExecutorType2.Worker,
  startDateTime: 52,
  terminationDateTime: 56,
  executorState: ExecutorState3.Creating,
  executorSize: 222,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



