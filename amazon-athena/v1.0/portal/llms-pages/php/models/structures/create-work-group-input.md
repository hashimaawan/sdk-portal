# Create Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type array.*


# Class Name

`CreateWorkGroupInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getName(): string | setName(string name): void |
| `configuration` | [`?Configuration`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/configuration.md) | Optional | - | getConfiguration(): ?Configuration | setConfiguration(?Configuration configuration): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `tags` | [`?(Tag[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/tag.md) | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreateWorkGroupInputBuilder;
use AmazonAthenaLib\Models\Builders\ConfigurationBuilder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1;
use AmazonAthenaLib\Models\Builders\TagBuilder;

$createWorkGroupInput = CreateWorkGroupInputBuilder::init(
    'Name6'
)
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
    ->description('Description0')
    ->tags(
        [
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



