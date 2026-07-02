# Result Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24x


# Interface Name

`ResultConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `outputLocation` | `string \| undefined` | Optional | - |
| `encryptionConfiguration` | [`EncryptionConfiguration2 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/encryption-configuration-2.md) | Optional | - |
| `expectedBucketOwner` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` |
| `aclConfiguration` | [`AclConfiguration1 \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/acl-configuration-1.md) | Optional | - |


# Example

```ts
import {
  EncryptionOption1Enum,
  ResultConfiguration1,
  S3AclOption1Enum,
} from 'amazon-athenalib';

const resultConfiguration1: ResultConfiguration1 = {
  outputLocation: 'OutputLocation4',
  encryptionConfiguration: {
    encryptionOption: EncryptionOption1Enum.SSES3,
    kmsKey: 'KmsKey6',
  },
  expectedBucketOwner: 'ExpectedBucketOwner4',
  aclConfiguration: {
    s3AclOption: S3AclOption1Enum.BUCKETOWNERFULLCONTROL,
  },
};
```



