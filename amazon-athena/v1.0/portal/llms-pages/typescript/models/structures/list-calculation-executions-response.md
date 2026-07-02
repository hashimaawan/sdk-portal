# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ


# Interface Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `calculations` | [`CalculationSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |


# Example

```ts
import {
  CalculationExecutionState1Enum,
  ListCalculationExecutionsResponse,
} from 'amazon-athenalib';

const listCalculationExecutionsResponse: ListCalculationExecutionsResponse = {
  nextToken: 'NextToken8',
  calculations: [
    {
      calculationExecutionId: 'CalculationExecutionId0',
      description: 'Description2',
      status: {
        submissionDateTime: '2016-03-13T12:52:32.123Z',
        completionDateTime: '2016-03-13T12:52:32.123Z',
        state: CalculationExecutionState1Enum.CANCELING,
        stateChangeReason: 'StateChangeReason8',
      },
    }
  ],
};
```



