# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0

*This model accepts additional fields of type unknown.*


# Interface Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecution` | [`QueryExecution1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-execution-1.md) | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  GetQueryExecutionOutput,
  S3AclOption1,
  StatementType1,
} from 'amazon-athenalib';

const getQueryExecutionOutput: GetQueryExecutionOutput = {
  queryExecution: {
    queryExecutionId: 'QueryExecutionId0',
    query: 'Query6',
    statementType: StatementType1.Ddl,
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
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



