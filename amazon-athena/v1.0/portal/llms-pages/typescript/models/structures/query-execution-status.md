# Query Execution Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uU3RhdHVz

The completion date, current state, submission time, and state change reason (if applicable) for the query execution.


# Interface Name

`QueryExecutionStatus`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`QueryExecutionState1Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/query-execution-state-1.md) | Optional | - |
| `stateChangeReason` | `string \| undefined` | Optional | - |
| `submissionDateTime` | `string \| undefined` | Optional | - |
| `completionDateTime` | `string \| undefined` | Optional | - |
| `athenaError` | [`AthenaError2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/athena-error-2.md) | Optional | - |


# Example

```ts
import {
  QueryExecutionState1Enum,
  QueryExecutionStatus,
} from 'amazon-athenalib';

const queryExecutionStatus: QueryExecutionStatus = {
  state: QueryExecutionState1Enum.SUCCEEDED,
  stateChangeReason: 'StateChangeReason0',
  submissionDateTime: '2016-03-13T12:52:32.123Z',
  completionDateTime: '2016-03-13T12:52:32.123Z',
  athenaError: {
    errorCategory: 3,
    errorType: 128,
    retryable: false,
    errorMessage: 'ErrorMessage8',
  },
};
```



