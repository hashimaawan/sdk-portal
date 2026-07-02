# Work Group 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRldvcmtHcm91cDI


# Class Name

`WorkGroup2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getName(): string | setName(string name): void |
| `state` | [`?string(WorkGroupState3Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/work-group-state-3.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `configuration` | [`?Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/configuration.md) | Optional | - | getConfiguration(): ?Configuration | setConfiguration(?Configuration configuration): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `creationTime` | `?DateTime` | Optional | - | getCreationTime(): ?\DateTime | setCreationTime(?\DateTime creationTime): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\WorkGroup2Builder;
use AmazonAthenaLib\Models\WorkGroupState3Enum;
use AmazonAthenaLib\Models\Builders\ConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;
use AmazonAthenaLib\Utils\DateTimeHelper;

$workGroup2 = WorkGroup2Builder::init(
    'Name0'
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
    ->description('Description6')
    ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->build();
```



