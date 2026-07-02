# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA

*This model accepts additional fields of type array.*


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroup` | [`?WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/work-group-2.md) | Optional | - | getWorkGroup(): ?WorkGroup2 | setWorkGroup(?WorkGroup2 workGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetWorkGroupOutputBuilder;
use AmazonAthenaLib\Models\Builders\WorkGroup2Builder;
use AmazonAthenaLib\Models\WorkGroupState3;
use AmazonAthenaLib\Models\Builders\ConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1;
use AmazonAthenaLib\Utils\DateTimeHelper;

$getWorkGroupOutput = GetWorkGroupOutputBuilder::init()
    ->workGroup(
        WorkGroup2Builder::init(
            'Name2'
        )
            ->state(WorkGroupState3::ENABLED)
            ->configuration(
                ConfigurationBuilder::init()
                    ->resultConfiguration(
                        ResultConfiguration1Builder::init()
                            ->outputLocation('OutputLocation0')
                            ->encryptionConfiguration(
                                EncryptionConfiguration2Builder::init(
                                    EncryptionOption1::SSE_S3
                                )
                                    ->kmsKey('KmsKey6')
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            )
                            ->expectedBucketOwner('ExpectedBucketOwner0')
                            ->aclConfiguration(
                                AclConfiguration1Builder::init(
                                    S3AclOption1::BUCKET_OWNER_FULL_CONTROL
                                )
                                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                                    ->build()
                            )
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->enforceWorkGroupConfiguration(false)
                    ->publishCloudWatchMetricsEnabled(false)
                    ->bytesScannedCutoffPerQuery(10000000)
                    ->requesterPaysEnabled(false)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->description('Description4')
            ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



