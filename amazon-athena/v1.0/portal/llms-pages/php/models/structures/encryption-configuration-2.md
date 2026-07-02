# Encryption Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9uMg


# Class Name

`EncryptionConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `encryptionOption` | [`string(EncryptionOption1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/encryption-option-1.md) | Required | - | getEncryptionOption(): string | setEncryptionOption(string encryptionOption): void |
| `kmsKey` | `?string` | Optional | - | getKmsKey(): ?string | setKmsKey(?string kmsKey): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;

$encryptionConfiguration2 = EncryptionConfiguration2Builder::init(
    EncryptionOption1Enum::SSE_S3
)
    ->kmsKey('KmsKey2')
    ->build();
```



