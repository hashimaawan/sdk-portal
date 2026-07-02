# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.

*This model accepts additional fields of type unknown.*


# Interface Name

`ResultConfigurationUpdates`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `outputLocation` | `string \| undefined` | Optional | - |
| `removeOutputLocation` | `boolean \| undefined` | Optional | - |
| `encryptionConfiguration` | [`EncryptionConfiguration2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/encryption-configuration-2.md) | Optional | - |
| `removeEncryptionConfiguration` | `boolean \| undefined` | Optional | - |
| `expectedBucketOwner` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `removeExpectedBucketOwner` | `boolean \| undefined` | Optional | - |
| `aclConfiguration` | [`AclConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/acl-configuration-1.md) | Optional | - |
| `removeAclConfiguration` | `boolean \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import {
  EncryptionOption1,
  ResultConfigurationUpdates,
} from 'amazon-athenalib';

const resultConfigurationUpdates: ResultConfigurationUpdates = {
  outputLocation: 'OutputLocation6',
  removeOutputLocation: false,
  encryptionConfiguration: {
    encryptionOption: EncryptionOption1.SseS3,
    kmsKey: 'KmsKey6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  removeEncryptionConfiguration: false,
  expectedBucketOwner: 'ExpectedBucketOwner6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



