# Result Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdENvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type array.*


# Class Name

`ResultConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `outputLocation` | `?string` | Optional | - | getOutputLocation(): ?string | setOutputLocation(?string outputLocation): void |
| `encryptionConfiguration` | [`?EncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/encryption-configuration-2.md) | Optional | - | getEncryptionConfiguration(): ?EncryptionConfiguration2 | setEncryptionConfiguration(?EncryptionConfiguration2 encryptionConfiguration): void |
| `expectedBucketOwner` | `?string` | Optional | **Constraints**: *Minimum Length*: `12`, *Maximum Length*: `12`, *Pattern*: `^[0-9]+$` | getExpectedBucketOwner(): ?string | setExpectedBucketOwner(?string expectedBucketOwner): void |
| `aclConfiguration` | [`?AclConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/acl-configuration-1.md) | Optional | - | getAclConfiguration(): ?AclConfiguration1 | setAclConfiguration(?AclConfiguration1 aclConfiguration): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1;

$resultConfiguration1 = ResultConfiguration1Builder::init()
    ->outputLocation('OutputLocation4')
    ->encryptionConfiguration(
        EncryptionConfiguration2Builder::init(
            EncryptionOption1::SSE_S3
        )
            ->kmsKey('KmsKey6')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->expectedBucketOwner('ExpectedBucketOwner4')
    ->aclConfiguration(
        AclConfiguration1Builder::init(
            S3AclOption1::BUCKET_OWNER_FULL_CONTROL
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



