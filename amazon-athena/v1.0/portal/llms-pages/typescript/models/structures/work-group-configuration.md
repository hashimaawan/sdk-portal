# Work Group Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb24

The configuration of the workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query and calculation results, whether the Amazon CloudWatch Metrics are enabled for the workgroup and whether workgroup settings override query settings, and the data usage limits for the amount of data scanned per query or per workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type unknown.*


# Interface Name

`WorkGroupConfiguration`


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
  S3AclOption1,
  WorkGroupConfiguration,
} from 'amazon-athenalib';

const workGroupConfiguration: WorkGroupConfiguration = {
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



