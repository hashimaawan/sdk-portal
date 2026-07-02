# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0


# Interface Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `executorStateFilter` | [`ExecutorState1Enum \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/executor-state-1.md) | Optional | - |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |


# Example

```ts
import { ExecutorState1Enum, ListExecutorsRequest } from 'amazon-athenalib';

const listExecutorsRequest: ListExecutorsRequest = {
  sessionId: 'SessionId0',
  executorStateFilter: ExecutorState1Enum.CREATING,
  maxResults: 100,
  nextToken: 'NextToken8',
};
```



