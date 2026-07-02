# Work Group

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRldvcmtHcm91cA

A workgroup, which contains a name, description, creation time, state, and other configuration, listed under <a>WorkGroup$Configuration</a>. Each workgroup enables you to isolate queries for you or your group of users from other queries in the same account, to configure the query results location and the encryption configuration (known as workgroup settings), to enable sending query metrics to Amazon CloudWatch, and to establish per-query data usage control limits for all queries in a workgroup. The workgroup settings override is specified in <code>EnforceWorkGroupConfiguration</code> (true/false) in the <code>WorkGroupConfiguration</code>. See <a>WorkGroupConfiguration$EnforceWorkGroupConfiguration</a>.

*This model accepts additional fields of type array.*


# Class Name

`WorkGroup`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getName(): string | setName(string name): void |
| `state` | [`?string(WorkGroupState3)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/work-group-state-3.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `configuration` | [`?Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/configuration.md) | Optional | - | getConfiguration(): ?Configuration | setConfiguration(?Configuration configuration): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `creationTime` | `?DateTime` | Optional | - | getCreationTime(): ?\DateTime | setCreationTime(?\DateTime creationTime): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\WorkGroupBuilder;
use AmazonAthenaLib\Models\WorkGroupState3;
use AmazonAthenaLib\Models\Builders\ConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1;
use AmazonAthenaLib\Utils\DateTimeHelper;

$workGroup = WorkGroupBuilder::init(
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
    ->description('Description6')
    ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



