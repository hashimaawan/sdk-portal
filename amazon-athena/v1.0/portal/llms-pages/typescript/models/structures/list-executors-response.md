# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ


# Interface Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `executorsSummary` | [`ExecutorsSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/executors-summary.md) | Optional | - |


# Example

```ts
import {
  ExecutorState3Enum,
  ExecutorType2Enum,
  ListExecutorsResponse,
} from 'amazon-athenalib';

const listExecutorsResponse: ListExecutorsResponse = {
  sessionId: 'SessionId4',
  nextToken: 'NextToken4',
  executorsSummary: [
    {
      executorId: 'ExecutorId8',
      executorType: ExecutorType2Enum.GATEWAY,
      startDateTime: 128,
      terminationDateTime: 236,
      executorState: ExecutorState3Enum.TERMINATED,
      executorSize: 42,
    },
    {
      executorId: 'ExecutorId8',
      executorType: ExecutorType2Enum.GATEWAY,
      startDateTime: 128,
      terminationDateTime: 236,
      executorState: ExecutorState3Enum.TERMINATED,
      executorSize: 42,
    },
    {
      executorId: 'ExecutorId8',
      executorType: ExecutorType2Enum.GATEWAY,
      startDateTime: 128,
      terminationDateTime: 236,
      executorState: ExecutorState3Enum.TERMINATED,
      executorSize: 42,
    }
  ],
};
```



