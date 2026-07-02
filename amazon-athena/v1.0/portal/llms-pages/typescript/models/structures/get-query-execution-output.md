# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0


# Interface Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecution` | [`QueryExecution1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-execution-1.md) | Optional | - |


# Example

```ts
import {
  EncryptionOption1Enum,
  GetQueryExecutionOutput,
  S3AclOption1Enum,
  StatementType1Enum,
} from 'amazon-athenalib';

const getQueryExecutionOutput: GetQueryExecutionOutput = {
  queryExecution: {
    queryExecutionId: 'QueryExecutionId0',
    query: 'Query6',
    statementType: StatementType1Enum.DDL,
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
};
```



