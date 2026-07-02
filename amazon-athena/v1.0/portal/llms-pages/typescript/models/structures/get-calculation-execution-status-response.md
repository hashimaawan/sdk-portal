# Get Calculation Execution Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uU3RhdHVzUmVzcG9uc2U


# Interface Name

`GetCalculationExecutionStatusResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status` | [`Status1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status-1.md) | Optional | - |
| `statistics` | [`Statistics1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/statistics-1.md) | Optional | - |


# Example

```ts
import {
  CalculationExecutionState1Enum,
  GetCalculationExecutionStatusResponse,
} from 'amazon-athenalib';

const getCalculationExecutionStatusResponse: GetCalculationExecutionStatusResponse = {
  status: {
    submissionDateTime: '2016-03-13T12:52:32.123Z',
    completionDateTime: '2016-03-13T12:52:32.123Z',
    state: CalculationExecutionState1Enum.CANCELING,
    stateChangeReason: 'StateChangeReason8',
  },
  statistics: {
    dpuExecutionInMillis: 164,
    progress: 'Progress6',
  },
};
```



