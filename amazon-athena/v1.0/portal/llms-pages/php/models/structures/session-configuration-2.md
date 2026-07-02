# Session Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlNlc3Npb25Db25maWd1cmF0aW9uMg


# Class Name

`SessionConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `executionRole` | `?string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | getExecutionRole(): ?string | setExecutionRole(?string executionRole): void |
| `workingDirectory` | `?string` | Optional | - | getWorkingDirectory(): ?string | setWorkingDirectory(?string workingDirectory): void |
| `idleTimeoutSeconds` | `?int` | Optional | - | getIdleTimeoutSeconds(): ?int | setIdleTimeoutSeconds(?int idleTimeoutSeconds): void |
| `encryptionConfiguration` | [`?EncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/encryption-configuration.md) | Optional | If query and calculation results are encrypted in Amazon S3, indicates the encryption option used (for example, <code>SSE_KMS</code> or <code>CSE_KMS</code>) and key information. | getEncryptionConfiguration(): ?EncryptionConfiguration | setEncryptionConfiguration(?EncryptionConfiguration encryptionConfiguration): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\SessionConfiguration2Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfigurationBuilder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;

$sessionConfiguration2 = SessionConfiguration2Builder::init()
    ->executionRole('ExecutionRole0')
    ->workingDirectory('WorkingDirectory4')
    ->idleTimeoutSeconds(82)
    ->encryptionConfiguration(
        EncryptionConfigurationBuilder::init(
            EncryptionOption1Enum::SSE_S3
        )
            ->kmsKey('KmsKey6')
            ->build()
    )
    ->build();
```



