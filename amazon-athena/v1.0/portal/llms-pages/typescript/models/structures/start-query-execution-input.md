# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA


# Interface Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `clientRequestToken` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `queryExecutionContext` | [`QueryExecutionContext1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-execution-context-1.md) | Optional | - |
| `resultConfiguration` | [`ResultConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-configuration-1.md) | Optional | - |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `executionParameters` | `string[] \| undefined` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `resultReuseConfiguration` | [`ResultReuseConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-reuse-configuration-1.md) | Optional | - |


# Example

```ts
import {
  EncryptionOption1Enum,
  S3AclOption1Enum,
  StartQueryExecutionInput,
} from 'amazon-athenalib';

const startQueryExecutionInput: StartQueryExecutionInput = {
  queryString: 'QueryString4',
  clientRequestToken: 'ClientRequestToken6',
  queryExecutionContext: {
    database: 'Database4',
    catalog: 'Catalog0',
  },
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
  workGroup: 'WorkGroup4',
  executionParameters: [
    'ExecutionParameters8'
  ],
};
```



