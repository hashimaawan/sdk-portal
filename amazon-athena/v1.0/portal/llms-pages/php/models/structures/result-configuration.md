# Result Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24

The location in Amazon S3 where query and calculation results are stored and the encryption option, if any, used for query and calculation results. These are known as "client-side settings". If workgroup settings override client-side settings, then the query uses the workgroup settings.


# Class Name

`ResultConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `outputLocation` | `?string` | Optional | - | getOutputLocation(): ?string | setOutputLocation(?string outputLocation): void |
| `encryptionConfiguration` | [`?EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/encryption-configuration-2.md) | Optional | - | getEncryptionConfiguration(): ?EncryptionConfiguration2 | setEncryptionConfiguration(?EncryptionConfiguration2 encryptionConfiguration): void |
| `expectedBucketOwner` | `?string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` | getExpectedBucketOwner(): ?string | setExpectedBucketOwner(?string expectedBucketOwner): void |
| `aclConfiguration` | [`?AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/acl-configuration-1.md) | Optional | - | getAclConfiguration(): ?AclConfiguration1 | setAclConfiguration(?AclConfiguration1 aclConfiguration): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;

$resultConfiguration = ResultConfigurationBuilder::init()
    ->outputLocation('OutputLocation4')
    ->encryptionConfiguration(
        EncryptionConfiguration2Builder::init(
            EncryptionOption1Enum::SSE_S3
        )
            ->kmsKey('KmsKey6')
            ->build()
    )
    ->expectedBucketOwner('ExpectedBucketOwner4')
    ->aclConfiguration(
        AclConfiguration1Builder::init(
            S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
        )->build()
    )->build();
```



