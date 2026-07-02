# Customer Content Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/typescript/x-redirect/JTI0bSUyRkN1c3RvbWVyQ29udGVudEVuY3J5cHRpb25Db25maWd1cmF0aW9u

Specifies the KMS key that is used to encrypt the user's data stores in Athena.

*This model accepts additional fields of type unknown.*


# Interface Name

`CustomerContentEncryptionConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `kmsKey` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:key/?[a-zA-Z_0-9+=,.@\-_/]+$\|^arn:aws[a-z\-]*:kms:([a-z0-9\-]+):\d{12}:alias/?[a-zA-Z_0-9+=,.@\-_/]+$\|^alias/[a-zA-Z0-9/_-]+$\|[a-f0-9]{8}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{4}-[a-f0-9]{12}` |
| `additionalProperties` | `Record<string, unknown>` | Optional | - |


# Example

```ts
import { CustomerContentEncryptionConfiguration } from 'amazon-athenalib';

const customerContentEncryptionConfiguration: CustomerContentEncryptionConfiguration = {
  kmsKey: 'KmsKey2',
  additionalProperties: {
    'exampleAdditionalProperty': { 'key1': 'val1', 'key2': 'val2' }
  },
};
```



