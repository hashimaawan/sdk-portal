# Session Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9uMg


# Interface Name

`SessionConfiguration2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `executionRole` | `string \| undefined` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` |
| `workingDirectory` | `string \| undefined` | Optional | - |
| `idleTimeoutSeconds` | `number \| undefined` | Optional | - |
| `encryptionConfiguration` | [`EncryptionConfiguration \| undefined`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/typescript/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. |


# Example

```ts
import {
  EncryptionOption1Enum,
  SessionConfiguration2,
} from 'amazon-athenalib';

const sessionConfiguration2: SessionConfiguration2 = {
  executionRole: 'ExecutionRole0',
  workingDirectory: 'WorkingDirectory4',
  idleTimeoutSeconds: 82,
  encryptionConfiguration: {
    encryptionOption: EncryptionOption1Enum.SSES3,
    kmsKey: 'KmsKey6',
  },
};
```



