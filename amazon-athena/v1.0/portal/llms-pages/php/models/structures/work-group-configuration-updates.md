# Work Group Configuration Updates

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRldvcmtHcm91cENvbmZpZ3VyYXRpb25VcGRhdGVz

The configuration information that will be updated for this workgroup, which includes the location in Amazon S3 where query and calculation results are stored, the encryption option, if any, used for query results, whether the Amazon CloudWatch Metrics are enabled for the workgroup, whether the workgroup settings override the client-side settings, and the data usage limit for the amount of bytes scanned per query, if it is specified.

*This model accepts additional fields of type array.*


# Class Name

`WorkGroupConfigurationUpdates`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enforceWorkGroupConfiguration` | `?bool` | Optional | - | getEnforceWorkGroupConfiguration(): ?bool | setEnforceWorkGroupConfiguration(?bool enforceWorkGroupConfiguration): void |
| `resultConfigurationUpdates` | [`?ResultConfigurationUpdates2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-configuration-updates-2.md) | Optional | - | getResultConfigurationUpdates(): ?ResultConfigurationUpdates2 | setResultConfigurationUpdates(?ResultConfigurationUpdates2 resultConfigurationUpdates): void |
| `publishCloudWatchMetricsEnabled` | `?bool` | Optional | - | getPublishCloudWatchMetricsEnabled(): ?bool | setPublishCloudWatchMetricsEnabled(?bool publishCloudWatchMetricsEnabled): void |
| `bytesScannedCutoffPerQuery` | `?int` | Optional | **Constraints**: `>= 10000000` | getBytesScannedCutoffPerQuery(): ?int | setBytesScannedCutoffPerQuery(?int bytesScannedCutoffPerQuery): void |
| `removeBytesScannedCutoffPerQuery` | `?bool` | Optional | - | getRemoveBytesScannedCutoffPerQuery(): ?bool | setRemoveBytesScannedCutoffPerQuery(?bool removeBytesScannedCutoffPerQuery): void |
| `requesterPaysEnabled` | `?bool` | Optional | - | getRequesterPaysEnabled(): ?bool | setRequesterPaysEnabled(?bool requesterPaysEnabled): void |
| `engineVersion` | [`?EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-version-1.md) | Optional | - | getEngineVersion(): ?EngineVersion1 | setEngineVersion(?EngineVersion1 engineVersion): void |
| `removeCustomerContentEncryptionConfiguration` | `?bool` | Optional | - | getRemoveCustomerContentEncryptionConfiguration(): ?bool | setRemoveCustomerContentEncryptionConfiguration(?bool removeCustomerContentEncryptionConfiguration): void |
| `additionalConfiguration` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getAdditionalConfiguration(): ?string | setAdditionalConfiguration(?string additionalConfiguration): void |
| `executionRole` | `?string` | Optional | **Constraints**: *Minimum Length*: `20`, *Maximum Length*: `2048`, *Pattern*: `^arn:aws[a-z\-]*:iam::\d{12}:role/?[a-zA-Z_0-9+=,.@\-_/]+$` | getExecutionRole(): ?string | setExecutionRole(?string executionRole): void |
| `customerContentEncryptionConfiguration` | [`?CustomerContentEncryptionConfiguration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/customer-content-encryption-configuration.md) | Optional | Specifies the KMS key that is used to encrypt the user's data stores in Athena. | getCustomerContentEncryptionConfiguration(): ?CustomerContentEncryptionConfiguration | setCustomerContentEncryptionConfiguration(?CustomerContentEncryptionConfiguration customerContentEncryptionConfiguration): void |
| `enableMinimumEncryptionConfiguration` | `?bool` | Optional | - | getEnableMinimumEncryptionConfiguration(): ?bool | setEnableMinimumEncryptionConfiguration(?bool enableMinimumEncryptionConfiguration): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\WorkGroupConfigurationUpdatesBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfigurationUpdates2Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;

$workGroupConfigurationUpdates = WorkGroupConfigurationUpdatesBuilder::init()
    ->enforceWorkGroupConfiguration(false)
    ->resultConfigurationUpdates(
        ResultConfigurationUpdates2Builder::init()
            ->outputLocation('OutputLocation0')
            ->removeOutputLocation(false)
            ->encryptionConfiguration(
                EncryptionConfiguration2Builder::init(
                    EncryptionOption1::SSE_S3
                )
                    ->kmsKey('KmsKey6')
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->removeEncryptionConfiguration(false)
            ->expectedBucketOwner('ExpectedBucketOwner0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->publishCloudWatchMetricsEnabled(false)
    ->bytesScannedCutoffPerQuery(10000000)
    ->removeBytesScannedCutoffPerQuery(false)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



