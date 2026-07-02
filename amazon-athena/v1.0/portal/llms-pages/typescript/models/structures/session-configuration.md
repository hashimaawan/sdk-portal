# Session Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9u

Contains session configuration information.

*This model accepts additional fields of type unknown.*


# Interface Name

`SessionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executionRole` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `workingDirectory` | `string \| undefined` | Optional | - |
| `idleTimeoutSeconds` | `number \| undefined` | Optional | - |
| `encryptionConfiguration` | [`EncryptionConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { EncryptionOption1, SessionConfiguration } from 'amazon-athenalib';

const sessionConfiguration: SessionConfiguration = {
  executionRole: 'ExecutionRole2',
  workingDirectory: 'WorkingDirectory6',
  idleTimeoutSeconds: 188,
  encryptionConfiguration: {
    encryptionOption: EncryptionOption1.SseS3,
    kmsKey: 'KmsKey6',
    additionalProperties: {
      'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
    },
  },
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



