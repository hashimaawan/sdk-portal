# Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5RXhlY3V0aW9uT3V0cHV0

*This model accepts additional fields of type array.*


# Class Name

`GetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecution` | [`?QueryExecution1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-execution-1.md) | Optional | - | getQueryExecution(): ?QueryExecution1 | setQueryExecution(?QueryExecution1 queryExecution): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryExecutionOutputBuilder;
use AmazonAthenaLib\Models\Builders\QueryExecution1Builder;
use AmazonAthenaLib\Models\StatementType1;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1;
use AmazonAthenaLib\Models\Builders\ResultReuseConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfiguration2Builder;

$getQueryExecutionOutput = GetQueryExecutionOutputBuilder::init()
    ->queryExecution(
        QueryExecution1Builder::init()
            ->queryExecutionId('QueryExecutionId0')
            ->query('Query6')
            ->statementType(StatementType1::DDL)
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
            ->resultReuseConfiguration(
                ResultReuseConfiguration1Builder::init()
                    ->resultReuseByAgeConfiguration(
                        ResultReuseByAgeConfiguration2Builder::init(
                            false
                        )
                            ->maxAgeInMinutes(26)
                            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                            ->build()
                    )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



