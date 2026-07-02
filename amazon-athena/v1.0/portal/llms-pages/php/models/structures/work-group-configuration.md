# Work Group Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb24

The configuration of the workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query and calculation results, whether the Amazon CloudWatch Metrics are enabled for the workgroup and whether workgroup settings override query settings, and the data usage limits for the amount of data scanned per query or per workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.


# Class Name

`WorkGroupConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resultConfiguration` | [`?ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-configuration-1.md) | Optional | - | getResultConfiguration(): ?ResultConfiguration1 | setResultConfiguration(?ResultConfiguration1 resultConfiguration): void |
| `enforceWorkGroupConfiguration` | `?bool` | Optional | - | getEnforceWorkGroupConfiguration(): ?bool | setEnforceWorkGroupConfiguration(?bool enforceWorkGroupConfiguration): void |
| `publishCloudWatchMetricsEnabled` | `?bool` | Optional | - | getPublishCloudWatchMetricsEnabled(): ?bool | setPublishCloudWatchMetricsEnabled(?bool publishCloudWatchMetricsEnabled): void |
| `bytesScannedCutoffPerQuery` | `?int` | Optional | **Constraints**: `>= 10000000` | getBytesScannedCutoffPerQuery(): ?int | setBytesScannedCutoffPerQuery(?int bytesScannedCutoffPerQuery): void |
| `requesterPaysEnabled` | `?bool` | Optional | - | getRequesterPaysEnabled(): ?bool | setRequesterPaysEnabled(?bool requesterPaysEnabled): void |
| `engineVersion` | [`?EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-version-1.md) | Optional | - | getEngineVersion(): ?EngineVersion1 | setEngineVersion(?EngineVersion1 engineVersion): void |
| `additionalConfiguration` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getAdditionalConfiguration(): ?string | setAdditionalConfiguration(?string additionalConfiguration): void |
| `executionRole` | `?string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | getExecutionRole(): ?string | setExecutionRole(?string executionRole): void |
| `customerContentEncryptionConfiguration` | [`?CustomerContentEncryptionConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/customer-content-encryption-configuration-2.md) | Optional | - | getCustomerContentEncryptionConfiguration(): ?CustomerContentEncryptionConfiguration2 | setCustomerContentEncryptionConfiguration(?CustomerContentEncryptionConfiguration2 customerContentEncryptionConfiguration): void |
| `enableMinimumEncryptionConfiguration` | `?bool` | Optional | - | getEnableMinimumEncryptionConfiguration(): ?bool | setEnableMinimumEncryptionConfiguration(?bool enableMinimumEncryptionConfiguration): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\WorkGroupConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;

$workGroupConfiguration = WorkGroupConfigurationBuilder::init()
    ->resultConfiguration(
        ResultConfiguration1Builder::init()
            ->outputLocation('OutputLocation0')
            ->encryptionConfiguration(
                EncryptionConfiguration2Builder::init(
                    EncryptionOption1Enum::SSE_S3
                )
                    ->kmsKey('KmsKey6')
                    ->build()
            )
            ->expectedBucketOwner('ExpectedBucketOwner0')
            ->aclConfiguration(
                AclConfiguration1Builder::init(
                    S3AclOption1Enum::BUCKET_OWNER_FULL_CONTROL
                )->build()
            )->build()
    )
    ->enforceWorkGroupConfiguration(false)
    ->publishCloudWatchMetricsEnabled(false)
    ->bytesScannedCutoffPerQuery(10000000)
    ->requesterPaysEnabled(false)
    ->build();
```



