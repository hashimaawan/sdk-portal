# Batch Get Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25JbnB1dA

Contains an array of query execution IDs.

*This model accepts additional fields of type unknown.*


# Interface Name

`BatchGetQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionIds` | `string[]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { BatchGetQueryExecutionInput } from 'amazon-athenalib';

const batchGetQueryExecutionInput: BatchGetQueryExecutionInput = {
  queryExecutionIds: [
    'QueryExecutionIds7',
    'QueryExecutionIds8',
    'QueryExecutionIds9'
  ],
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



