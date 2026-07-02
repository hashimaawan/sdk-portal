# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ


# Interface Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `preparedStatements` | [`PreparedStatement[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/prepared-statement.md) | Optional | - |
| `unprocessedPreparedStatementNames` | [`UnprocessedPreparedStatementName[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/unprocessed-prepared-statement-name.md) | Optional | - |


# Example

```ts
import { BatchGetPreparedStatementOutput } from 'amazon-athenalib';

const batchGetPreparedStatementOutput: BatchGetPreparedStatementOutput = {
  preparedStatements: [
    {
      statementName: 'StatementName2',
      queryStatement: 'QueryStatement6',
      workGroupName: 'WorkGroupName6',
      description: 'Description2',
      lastModifiedTime: '2016-03-13T12:52:32.123Z',
    },
    {
      statementName: 'StatementName2',
      queryStatement: 'QueryStatement6',
      workGroupName: 'WorkGroupName6',
      description: 'Description2',
      lastModifiedTime: '2016-03-13T12:52:32.123Z',
    }
  ],
  unprocessedPreparedStatementNames: [
    {
      statementName: 'StatementName0',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
    },
    {
      statementName: 'StatementName0',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
    },
    {
      statementName: 'StatementName0',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
    }
  ],
};
```



