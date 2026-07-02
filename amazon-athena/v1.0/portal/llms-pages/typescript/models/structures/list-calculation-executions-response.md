# List Calculation Executions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListCalculationExecutionsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `calculations` | [`CalculationSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/calculation-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CalculationExecutionState1,
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
        state: CalculationExecutionState1.Canceling,
        stateChangeReason: 'StateChangeReason8',
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



