# Result Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb25VcGRhdGVz

The information about the updates in the query results, such as output location and encryption configuration for the query results.


# Class Name

`ResultConfigurationUpdates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `outputLocation` | `?string` | Optional | - | getOutputLocation(): ?string | setOutputLocation(?string outputLocation): void |
| `removeOutputLocation` | `?bool` | Optional | - | getRemoveOutputLocation(): ?bool | setRemoveOutputLocation(?bool removeOutputLocation): void |
| `encryptionConfiguration` | [`?EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/encryption-configuration-2.md) | Optional | - | getEncryptionConfiguration(): ?EncryptionConfiguration2 | setEncryptionConfiguration(?EncryptionConfiguration2 encryptionConfiguration): void |
| `removeEncryptionConfiguration` | `?bool` | Optional | - | getRemoveEncryptionConfiguration(): ?bool | setRemoveEncryptionConfiguration(?bool removeEncryptionConfiguration): void |
| `expectedBucketOwner` | `?string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` | getExpectedBucketOwner(): ?string | setExpectedBucketOwner(?string expectedBucketOwner): void |
| `removeExpectedBucketOwner` | `?bool` | Optional | - | getRemoveExpectedBucketOwner(): ?bool | setRemoveExpectedBucketOwner(?bool removeExpectedBucketOwner): void |
| `aclConfiguration` | [`?AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/acl-configuration-1.md) | Optional | - | getAclConfiguration(): ?AclConfiguration1 | setAclConfiguration(?AclConfiguration1 aclConfiguration): void |
| `removeAclConfiguration` | `?bool` | Optional | - | getRemoveAclConfiguration(): ?bool | setRemoveAclConfiguration(?bool removeAclConfiguration): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultConfigurationUpdatesBuilder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;

$resultConfigurationUpdates = ResultConfigurationUpdatesBuilder::init()
    ->outputLocation('OutputLocation6')
    ->removeOutputLocation(false)
    ->encryptionConfiguration(
        EncryptionConfiguration2Builder::init(
            EncryptionOption1Enum::SSE_S3
        )
            ->kmsKey('KmsKey6')
            ->build()
    )
    ->removeEncryptionConfiguration(false)
    ->expectedBucketOwner('ExpectedBucketOwner6')
    ->build();
```



