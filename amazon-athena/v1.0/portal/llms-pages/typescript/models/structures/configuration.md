# Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb24

*This model accepts additional fields of type unknown.*


# Interface Name

`MConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `resultConfiguration` | [`ResultConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-configuration-1.md) | Optional | - |
| `enforceWorkGroupConfiguration` | `boolean \| undefined` | Optional | - |
| `publishCloudWatchMetricsEnabled` | `boolean \| undefined` | Optional | - |
| `bytesScannedCutoffPerQuery` | `number \| undefined` | Optional | **Constraints**: `>= 10000000` |
| `requesterPaysEnabled` | `boolean \| undefined` | Optional | - |
| `engineVersion` | [`EngineVersion1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-version-1.md) | Optional | - |
| `additionalConfiguration` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `executionRole` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `customerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/customer-content-encryption-configuration-2.md) | Optional | - |
| `enableMinimumEncryptionConfiguration` | `boolean \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  MConfiguration,
  S3AclOption1,
} from 'amazon-athenalib';

const configuration: MConfiguration = {
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
  enforceWorkGroupConfiguration: false,
  publishCloudWatchMetricsEnabled: false,
  bytesScannedCutoffPerQuery: 10000000,
  requesterPaysEnabled: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



