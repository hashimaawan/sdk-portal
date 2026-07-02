# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXR1cw


# Interface Name

`Status`


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
import { QueryExecutionState1Enum, Status } from 'amazon-athenalib';

const status: Status = {
  state: QueryExecutionState1Enum.QUEUED,
  stateChangeReason: 'StateChangeReason8',
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



