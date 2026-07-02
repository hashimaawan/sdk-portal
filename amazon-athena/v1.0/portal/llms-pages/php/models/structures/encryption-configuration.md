# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `encryptionOption` | [`string(EncryptionOption1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/encryption-option-1.md) | Required | - | getEncryptionOption(): string | setEncryptionOption(string encryptionOption): void |
| `kmsKey` | `?string` | Optional | - | getKmsKey(): ?string | setKmsKey(?string kmsKey): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\EncryptionConfigurationBuilder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;

$encryptionConfiguration = EncryptionConfigurationBuilder::init(
    EncryptionOption1Enum::SSE_KMS
)
    ->kmsKey('KmsKey6')
    ->build();
```



