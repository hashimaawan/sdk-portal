# Unprocessed Query Execution Id

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlVucHJvY2Vzc2VkUXVlcnlFeGVjdXRpb25JZA

Describes a query execution that failed to process.

*This model accepts additional fields of type unknown.*


# Interface Name

`UnprocessedQueryExecutionId`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `errorCode` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` |
| `errorMessage` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { UnprocessedQueryExecutionId } from 'amazon-athenalib';

const unprocessedQueryExecutionId: UnprocessedQueryExecutionId = {
  queryExecutionId: 'QueryExecutionId6',
  errorCode: 'ErrorCode2',
  errorMessage: 'ErrorMessage8',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



