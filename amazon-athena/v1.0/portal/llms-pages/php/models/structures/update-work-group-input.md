# Update Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVwZGF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type array.*


# Class Name

`UpdateWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `configurationUpdates` | [`?ConfigurationUpdates`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/configuration-updates.md) | Optional | - | getConfigurationUpdates(): ?ConfigurationUpdates | setConfigurationUpdates(?ConfigurationUpdates configurationUpdates): void |
| `state` | [`?string(WorkGroupState2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/work-group-state-2.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UpdateWorkGroupInputBuilder;
use AmazonAthenaLib\Models\Builders\ConfigurationUpdatesBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfigurationUpdates2Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\WorkGroupState2;

$updateWorkGroupInput = UpdateWorkGroupInputBuilder::init(
    'WorkGroup0'
)
    ->description('Description8')
    ->configurationUpdates(
        ConfigurationUpdatesBuilder::init()
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
            ->build()
    )
    ->state(WorkGroupState2::ENABLED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



