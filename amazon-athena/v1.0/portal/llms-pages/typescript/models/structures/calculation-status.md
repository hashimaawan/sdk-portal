# Calculation Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3RhdHVz

Contains information about the status of a notebook calculation.

*This model accepts additional fields of type unknown.*


# Interface Name

`CalculationStatus`


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
import {
  CalculationExecutionState1,
  CalculationStatus,
} from 'amazon-athenalib';

const calculationStatus: CalculationStatus = {
  submissionDateTime: '2016-03-13T12:52:32.123Z',
  completionDateTime: '2016-03-13T12:52:32.123Z',
  state: CalculationExecutionState1.Creating,
  stateChangeReason: 'StateChangeReason2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



