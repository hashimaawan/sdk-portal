# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0


# Interface Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `stateFilter` | [`CalculationExecutionState3Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/calculation-execution-state-3.md) | Optional | - |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```ts
import {
  CalculationExecutionState3Enum,
  ListCalculationExecutionsRequest,
} from 'amazon-athenalib';

const listCalculationExecutionsRequest: ListCalculationExecutionsRequest = {
  sessionId: 'SessionId2',
  stateFilter: CalculationExecutionState3Enum.QUEUED,
  maxResults: 100,
  nextToken: 'NextToken0',
};
```



