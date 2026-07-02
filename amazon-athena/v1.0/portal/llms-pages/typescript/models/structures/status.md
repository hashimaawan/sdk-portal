# Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXR1cw

*This model accepts additional fields of type unknown.*


# Interface Name

`Status`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `state` | [`QueryExecutionState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/query-execution-state-1.md) | Optional | - |
| `stateChangeReason` | `string \| undefined` | Optional | - |
| `submissionDateTime` | `string \| undefined` | Optional | - |
| `completionDateTime` | `string \| undefined` | Optional | - |
| `athenaError` | [`AthenaError2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/athena-error-2.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { QueryExecutionState1, Status } from 'amazon-athenalib';

const status: Status = {
  state: QueryExecutionState1.Queued,
  stateChangeReason: 'StateChangeReason8',
  submissionDateTime: '2016-03-13T12:52:32.123Z',
  completionDateTime: '2016-03-13T12:52:32.123Z',
  athenaError: {
    errorCategory: 3,
    errorType: 128,
    retryable: false,
    errorMessage: 'ErrorMessage8',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



