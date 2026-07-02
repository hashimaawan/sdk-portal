# Work Group Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb25VcGRhdGVz

The configuration information that will be updated for this workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query results, whether the Amazon CloudWatch Metrics are enabled for the workgroup, whether the workgroup settings override the client-side settings, and the data usage limit for the amount of bytes scanned per query, if it is specified.

*This model accepts additional fields of type unknown.*


# Interface Name

`WorkGroupConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `enforceWorkGroupConfiguration` | `boolean \| undefined` | Optional | - |
| `resultConfigurationUpdates` | [`ResultConfigurationUpdates2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/result-configuration-updates-2.md) | Optional | - |
| `publishCloudWatchMetricsEnabled` | `boolean \| undefined` | Optional | - |
| `bytesScannedCutoffPerQuery` | `number \| undefined` | Optional | **Constraints**: `>= 10000000` |
| `removeBytesScannedCutoffPerQuery` | `boolean \| undefined` | Optional | - |
| `requesterPaysEnabled` | `boolean \| undefined` | Optional | - |
| `engineVersion` | [`EngineVersion1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/engine-version-1.md) | Optional | - |
| `removeCustomerContentEncryptionConfiguration` | `boolean \| undefined` | Optional | - |
| `additionalConfiguration` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `executionRole` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `customerContentEncryptionConfiguration` | [`CustomerContentEncryptionConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. |
| `enableMinimumEncryptionConfiguration` | `boolean \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  WorkGroupConfigurationUpdates,
} from 'amazon-athenalib';

const workGroupConfigurationUpdates: WorkGroupConfigurationUpdates = {
  enforceWorkGroupConfiguration: false,
  resultConfigurationUpdates: {
    outputLocation: 'OutputLocation0',
    removeOutputLocation: false,
    encryptionConfiguration: {
      encryptionOption: EncryptionOption1.SseS3,
      kmsKey: 'KmsKey6',
      additionalProperties: {
        'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
      },
    },
    removeEncryptionConfiguration: false,
    expectedBucketOwner: 'ExpectedBucketOwner0',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  publishCloudWatchMetricsEnabled: false,
  bytesScannedCutoffPerQuery: 10000000,
  removeBytesScannedCutoffPerQuery: false,
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



