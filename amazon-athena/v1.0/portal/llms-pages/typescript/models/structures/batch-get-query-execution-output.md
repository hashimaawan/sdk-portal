# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type unknown.*


# Interface Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutions` | [`QueryExecution[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-execution.md) | Optional | - |
| `unprocessedQueryExecutionIds` | [`UnprocessedQueryExecutionId[] \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/unprocessed-query-execution-id.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  BatchGetQueryExecutionOutput,
  EncryptionOption1,
  S3AclOption1,
  StatementType1,
} from 'amazon-athenalib';

const batchGetQueryExecutionOutput: BatchGetQueryExecutionOutput = {
  queryExecutions: [
    {
      queryExecutionId: 'QueryExecutionId6',
      query: 'Query0',
      statementType: StatementType1.Utility,
      resultConfiguration: {
        outputLocation: 'OutputLocation0',
        encryptionConfiguration: {
          encryptionOption: EncryptionOption1.SseS3,
          kmsKey: 'KmsKey6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        expectedBucketOwner: 'ExpectedBucketOwner0',
        aclConfiguration: {
          s3AclOption: S3AclOption1.BucketOwnerFullControl,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      resultReuseConfiguration: {
        resultReuseByAgeConfiguration: {
          enabled: false,
          maxAgeInMinutes: 26,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      queryExecutionId: 'QueryExecutionId6',
      query: 'Query0',
      statementType: StatementType1.Utility,
      resultConfiguration: {
        outputLocation: 'OutputLocation0',
        encryptionConfiguration: {
          encryptionOption: EncryptionOption1.SseS3,
          kmsKey: 'KmsKey6',
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        expectedBucketOwner: 'ExpectedBucketOwner0',
        aclConfiguration: {
          s3AclOption: S3AclOption1.BucketOwnerFullControl,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      resultReuseConfiguration: {
        resultReuseByAgeConfiguration: {
          enabled: false,
          maxAgeInMinutes: 26,
          additionalProperties: {
            'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
          },
        },
        additionalProperties: {
          'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
        },
      },
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    }
  ],
  unprocessedQueryExecutionIds: [
    {
      queryExecutionId: 'QueryExecutionId6',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      queryExecutionId: 'QueryExecutionId6',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    {
      queryExecutionId: 'QueryExecutionId6',
      errorCode: 'ErrorCode2',
      errorMessage: 'ErrorMessage8',
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



