# Query Execution

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9u

Information about a single instance of a query execution.

*This model accepts additional fields of type unknown.*


# Interface Name

`QueryExecution`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `queryExecutionId` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` |
| `query` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` |
| `statementType` | [`StatementType1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/statement-type-1.md) | Optional | - |
| `resultConfiguration` | [`ResultConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-configuration-1.md) | Optional | - |
| `resultReuseConfiguration` | [`ResultReuseConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-reuse-configuration-1.md) | Optional | - |
| `queryExecutionContext` | [`QueryExecutionContext1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/query-execution-context-1.md) | Optional | - |
| `status` | [`Status \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/status.md) | Optional | - |
| `statistics` | [`Statistics \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/statistics.md) | Optional | - |
| `workGroup` | `string \| undefined` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engineVersion` | [`EngineVersion1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-version-1.md) | Optional | - |
| `executionParameters` | `string[] \| undefined` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `substatementType` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  QueryExecution,
  S3AclOption1,
  StatementType1,
} from 'amazon-athenalib';

const queryExecution: QueryExecution = {
  queryExecutionId: 'QueryExecutionId4',
  query: 'Query2',
  statementType: StatementType1.Dml,
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
};
```



