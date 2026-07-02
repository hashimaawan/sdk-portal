# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0

*This model accepts additional fields of type unknown.*


# Interface Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `executorStateFilter` | [`ExecutorState1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/executor-state-1.md) | Optional | - |
| `maxResults` | `number \| undefined` | Optional | **Constraints**: `>= 1`, `<= 100` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { ExecutorState1, ListExecutorsRequest } from 'amazon-athenalib';

const listExecutorsRequest: ListExecutorsRequest = {
  sessionId: 'SessionId0',
  executorStateFilter: ExecutorState1.Creating,
  maxResults: 100,
  nextToken: 'NextToken8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



