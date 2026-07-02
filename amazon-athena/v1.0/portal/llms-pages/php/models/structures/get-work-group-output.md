# Get Work Group Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cE91dHB1dA


# Class Name

`GetWorkGroupOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroup` | [`?WorkGroup2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/work-group-2.md) | Optional | - | getWorkGroup(): ?WorkGroup2 | setWorkGroup(?WorkGroup2 workGroup): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetWorkGroupOutputBuilder;
use AmazonAthenaLib\Models\Builders\WorkGroup2Builder;
use AmazonAthenaLib\Models\WorkGroupState3Enum;
use AmazonAthenaLib\Models\Builders\ConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;
use AmazonAthenaLib\Utils\DateTimeHelper;

$getWorkGroupOutput = GetWorkGroupOutputBuilder::init()
    ->workGroup(
        WorkGroup2Builder::init(
            'Name2'
        )
            ->state(WorkGroupState3Enum::ENABLED)
            ->configuration(
                ConfigurationBuilder::init()
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
                    ->build()
            )
            ->description('Description4')
            ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->build()
    )
    ->build();
```



