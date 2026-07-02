# Encryption Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkVuY3J5cHRpb25Db25maWd1cmF0aW9u

If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information.

*This model accepts additional fields of type array.*


# Class Name

`EncryptionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `encryptionOption` | [`string(EncryptionOption1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/encryption-option-1.md) | Required | - | getEncryptionOption(): string | setEncryptionOption(string encryptionOption): void |
| `kmsKey` | `?string` | Optional | - | getKmsKey(): ?string | setKmsKey(?string kmsKey): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\EncryptionConfigurationBuilder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;

$encryptionConfiguration = EncryptionConfigurationBuilder::init(
    EncryptionOption1::SSE_KMS
)
    ->kmsKey('KmsKey6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



