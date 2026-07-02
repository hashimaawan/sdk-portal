# Result Configuration Updates 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVzMg


# Interface Name

`ResultConfigurationUpdates2`


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


# Example

```ts
import {
  EncryptionOption1Enum,
  ResultConfigurationUpdates2,
} from 'amazon-athenalib';

const resultConfigurationUpdates2: ResultConfigurationUpdates2 = {
  outputLocation: 'OutputLocation4',
  removeOutputLocation: false,
  encryptionConfiguration: {
    encryptionOption: EncryptionOption1Enum.SSES3,
    kmsKey: 'KmsKey6',
  },
  removeEncryptionConfiguration: false,
  expectedBucketOwner: 'ExpectedBucketOwner4',
};
```



