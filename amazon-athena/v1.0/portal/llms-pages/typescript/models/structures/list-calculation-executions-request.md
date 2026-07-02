# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `stateFilter` | [`CalculationExecutionState3 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  CalculationExecutionState3,
  ListCalculationExecutionsRequest,
} from 'amazon-athenalib';

const listCalculationExecutionsRequest: ListCalculationExecutionsRequest = {
  sessionId: 'SessionId2',
  stateFilter: CalculationExecutionState3.Queued,
  maxResults: 100,
  nextToken: 'NextToken0',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



