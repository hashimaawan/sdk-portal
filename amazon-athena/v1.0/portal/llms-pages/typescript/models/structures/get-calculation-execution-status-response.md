# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U

*This model accepts additional fields of type unknown.*


# Interface Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/statistics-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CalculationExecutionState1,
  GetCalculationExecutionStatusResponse,
} from 'amazon-athenalib';

const getCalculationExecutionStatusResponse: GetCalculationExecutionStatusResponse = {
  status: {
    submissionDateTime: '2016-03-13T12:52:32.123Z',
    completionDateTime: '2016-03-13T12:52:32.123Z',
    state: CalculationExecutionState1.Canceling,
    stateChangeReason: 'StateChangeReason8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  statistics: {
    dpuExecutionInMillis: 164,
    progress: 'Progress6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



