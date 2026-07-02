# Status 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXR1czE

*This model accepts additional fields of type unknown.*


# Interface Name

`Status1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `submissionDateTime` | `string \| undefined` | Optional | - |
| `completionDateTime` | `string \| undefined` | Optional | - |
| `state` | [`CalculationExecutionState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/calculation-execution-state-1.md) | Optional | - |
| `stateChangeReason` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CalculationExecutionState1, Status1 } from 'amazon-athenalib';

const status1: Status1 = {
  submissionDateTime: '2016-03-13T12:52:32.123Z',
  completionDateTime: '2016-03-13T12:52:32.123Z',
  state: CalculationExecutionState1.Queued,
  stateChangeReason: 'StateChangeReason0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



