# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Interface Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutions` | [`QueryExecution[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-execution.md) | Optional | - |
| `unprocessedQueryExecutionIds` | [`UnprocessedQueryExecutionId[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/unprocessed-query-execution-id.md) | Optional | - |


# Example

```ts
import {
  BatchGetQueryExecutionOutput,
  EncryptionOption1Enum,
  S3AclOption1Enum,
  StatementType1Enum,
} from 'amazon-athenalib';

const batchGetQueryExecutionOutput: BatchGetQueryExecutionOutput = {
  queryExecutions: [
    {
      queryExecutionId: 'QueryExecutionId6',
      query: 'Query0',
      statementType: StatementType1Enum.UTILITY,
      resultConfiguration: {
        outputLocation: 'OutputLocation0',
        encryptionConfiguration: {
          encryptionOption: EncryptionOption1Enum.SSES3,
          kmsKey: 'KmsKey6',
        },
        expectedBucketOwner: 'ExpectedBucketOwner0',
        aclConfiguration: {
          s3AclOption: S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
        },
      },
      resultReuseConfiguration: {
        resultReuseByAgeConfiguration: {
          enabled: false,
          maxAgeInMinutes: 26,
        },
      },
    },
    {
      queryExecutionId: 'QueryExecutionId6',
      query: 'Query0',
      statementType: StatementType1Enum.UTILITY,
      resultConfiguration: {
        outputLocation: 'OutputLocation0',
        encryptionConfiguration: {
          encryptionOption: EncryptionOption1Enum.SSES3,
          kmsKey: 'KmsKey6',
        },
        expectedBucketOwner: 'ExpectedBucketOwner0',
        aclConfiguration: {
          s3AclOption: S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
        },
      },
      resultReuseConfiguration: {
        resultReuseByAgeConfiguration: {
          enabled: false,
          maxAgeInMinutes: 26,
        },
      },
    }
  ],
  unprocessedQueryExecutionIds: [
    {
      queryExecutionId: 'QueryExecutionId6',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
    },
    {
      queryExecutionId: 'QueryExecutionId6',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
    },
    {
      queryExecutionId: 'QueryExecutionId6',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
    }
  ],
};
```



