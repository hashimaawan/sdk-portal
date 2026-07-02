# Session Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9u

Contains session configuration information.

*This model accepts additional fields of type array.*


# Class Name

`SessionConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `executionRole` | `?string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | getExecutionRole(): ?string | setExecutionRole(?string executionRole): void |
| `workingDirectory` | `?string` | Optional | - | getWorkingDirectory(): ?string | setWorkingDirectory(?string workingDirectory): void |
| `idleTimeoutSeconds` | `?int` | Optional | - | getIdleTimeoutSeconds(): ?int | setIdleTimeoutSeconds(?int idleTimeoutSeconds): void |
| `encryptionConfiguration` | [`?EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. | getEncryptionConfiguration(): ?EncryptionConfiguration | setEncryptionConfiguration(?EncryptionConfiguration encryptionConfiguration): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\SessionConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\EncryptionConfigurationBuilder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;

$sessionConfiguration = SessionConfigurationBuilder::init()
    ->executionRole('ExecutionRole2')
    ->workingDirectory('WorkingDirectory6')
    ->idleTimeoutSeconds(188)
    ->encryptionConfiguration(
        EncryptionConfigurationBuilder::init(
            EncryptionOption1::SSE_S3
        )
            ->kmsKey('KmsKey6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



