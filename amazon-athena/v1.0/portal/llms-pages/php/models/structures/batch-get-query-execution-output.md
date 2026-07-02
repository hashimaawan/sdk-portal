# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutions` | [`?(QueryExecution[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-execution.md) | Optional | - | getQueryExecutions(): ?array | setQueryExecutions(?array queryExecutions): void |
| `unprocessedQueryExecutionIds` | [`?(UnprocessedQueryExecutionId[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/unprocessed-query-execution-id.md) | Optional | - | getUnprocessedQueryExecutionIds(): ?array | setUnprocessedQueryExecutionIds(?array unprocessedQueryExecutionIds): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetQueryExecutionOutputBuilder;
use AmazonAthenaLib\Models\Builders\QueryExecutionBuilder;
use AmazonAthenaLib\Models\StatementType1;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1;
use AmazonAthenaLib\Models\Builders\ResultReuseConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfiguration2Builder;
use AmazonAthenaLib\Models\Builders\UnprocessedQueryExecutionIdBuilder;

$batchGetQueryExecutionOutput = BatchGetQueryExecutionOutputBuilder::init()
    ->queryExecutions(
        [
            QueryExecutionBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->query('Query0')
                ->statementType(StatementType1::UTILITY)
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
                ->build(),
            QueryExecutionBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->query('Query0')
                ->statementType(StatementType1::UTILITY)
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
        ]
    )
    ->unprocessedQueryExecutionIds(
        [
            UnprocessedQueryExecutionIdBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            UnprocessedQueryExecutionIdBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            UnprocessedQueryExecutionIdBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



