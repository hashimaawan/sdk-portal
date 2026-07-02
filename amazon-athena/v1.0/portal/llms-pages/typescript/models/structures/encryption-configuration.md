# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.

*This model accepts additional fields of type unknown.*


# Interface Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `encryptionOption` | [`EncryptionOption1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/enumerations/encryption-option-1.md) | Required | - |
| `kmsKey` | `string \| undefined` | Optional | - |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { EncryptionConfiguration, EncryptionOption1 } from 'amazon-athenalib';

const encryptionConfiguration: EncryptionConfiguration = {
  encryptionOption: EncryptionOption1.SseKms,
  kmsKey: 'KmsKey6',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



