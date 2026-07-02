# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg


# Interface Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encryptionOption` | [`EncryptionOption1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/encryption-option-1.md) | Required | - |
| `kmsKey` | `string \| undefined` | Optional | - |


# Example

```ts
import {
  EncryptionConfiguration2,
  EncryptionOption1Enum,
} from 'amazon-athenalib';

const encryptionConfiguration2: EncryptionConfiguration2 = {
  encryptionOption: EncryptionOption1Enum.SSES3,
  kmsKey: 'KmsKey2',
};
```



