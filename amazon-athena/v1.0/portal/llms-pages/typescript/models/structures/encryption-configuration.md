# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.


# Interface Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encryptionOption` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/encryption-option-1.md) | Required | - |
| `kmsKey` | `string \| undefined` | Optional | - |


# Example

```ts
import {
  EncryptionConfiguration,
  EncryptionOption1Enum,
} from 'amazon-athenalib';

const encryptionConfiguration: EncryptionConfiguration = {
  encryptionOption: EncryptionOption1Enum.SSEKMS,
  kmsKey: 'KmsKey6',
};
```



