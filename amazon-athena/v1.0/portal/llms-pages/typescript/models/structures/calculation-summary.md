# Calculation Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uU3VtbWFyeQ

Summary information for a notebook calculation.


# Interface Name

`CalculationSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `calculationExecutionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `36` |
| `description` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `status` | [`Status1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-1.md) | Optional | - |


# Example

```ts
import {
  CalculationExecutionState1Enum,
  CalculationSummary,
} from 'amazon-athenalib';

const calculationSummary: CalculationSummary = {
  calculationExecutionId: 'CalculationExecutionId4',
  description: 'Description6',
  status: {
    submissionDateTime: '2016-03-13T12:52:32.123Z',
    completionDateTime: '2016-03-13T12:52:32.123Z',
    state: CalculationExecutionState1Enum.CANCELING,
    stateChangeReason: 'StateChangeReason8',
  },
};
```



