# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ

*This model accepts additional fields of type unknown.*


# Interface Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `nextToken` | `string \| undefined` | Optional | **Constraints**: *Maximum Length*: `2048` |
| `executorsSummary` | [`ExecutorsSummary[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/executors-summary.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  ExecutorState3,
  ExecutorType2,
  ListExecutorsResponse,
} from 'amazon-athenalib';

const listExecutorsResponse: ListExecutorsResponse = {
  sessionId: 'SessionId4',
  nextToken: 'NextToken4',
  executorsSummary: [
    {
      executorId: 'ExecutorId8',
      executorType: ExecutorType2.Gateway,
      startDateTime: 128,
      terminationDateTime: 236,
      executorState: ExecutorState3.Terminated,
      executorSize: 42,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      executorId: 'ExecutorId8',
      executorType: ExecutorType2.Gateway,
      startDateTime: 128,
      terminationDateTime: 236,
      executorState: ExecutorState3.Terminated,
      executorSize: 42,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      executorId: 'ExecutorId8',
      executorType: ExecutorType2.Gateway,
      startDateTime: 128,
      terminationDateTime: 236,
      executorState: ExecutorState3.Terminated,
      executorSize: 42,
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



