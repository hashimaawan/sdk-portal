# Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkNvbmZpZ3VyYXRpb25VcGRhdGVz


# Interface Name

`ConfigurationUpdates`


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


# Example

```ts
import {
  ConfigurationUpdates,
  EncryptionOption1Enum,
} from 'amazon-athenalib';

const configurationUpdates: ConfigurationUpdates = {
  enforceWorkGroupConfiguration: false,
  resultConfigurationUpdates: {
    outputLocation: 'OutputLocation0',
    removeOutputLocation: false,
    encryptionConfiguration: {
      encryptionOption: EncryptionOption1Enum.SSES3,
      kmsKey: 'KmsKey6',
    },
    removeEncryptionConfiguration: false,
    expectedBucketOwner: 'ExpectedBucketOwner0',
  },
  publishCloudWatchMetricsEnabled: false,
  bytesScannedCutoffPerQuery: 10000000,
  removeBytesScannedCutoffPerQuery: false,
};
```



