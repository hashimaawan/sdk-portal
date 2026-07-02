# Batch Get Query Execution Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0UXVlcnlFeGVjdXRpb25PdXRwdXQ


# Class Name

`BatchGetQueryExecutionOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutions` | [`?(QueryExecution[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-execution.md) | Optional | - | getQueryExecutions(): ?array | setQueryExecutions(?array queryExecutions): void |
| `unprocessedQueryExecutionIds` | [`?(UnprocessedQueryExecutionId[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/unprocessed-query-execution-id.md) | Optional | - | getUnprocessedQueryExecutionIds(): ?array | setUnprocessedQueryExecutionIds(?array unprocessedQueryExecutionIds): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetQueryExecutionOutputBuilder;
use AmazonAthenaLib\Models\Builders\QueryExecutionBuilder;
use AmazonAthenaLib\Models\StatementType1Enum;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;
use AmazonAthenaLib\Models\Builders\ResultReuseConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfiguration2Builder;
use AmazonAthenaLib\Models\Builders\UnprocessedQueryExecutionIdBuilder;

$batchGetQueryExecutionOutput = BatchGetQueryExecutionOutputBuilder::init()
    ->queryExecutions(
        [
            QueryExecutionBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->query('Query0')
                ->statementType(StatementType1Enum::UTILITY)
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
                ->resultReuseConfiguration(
                    ResultReuseConfiguration1Builder::init()
                        ->resultReuseByAgeConfiguration(
                            ResultReuseByAgeConfiguration2Builder::init(
                                false
                            )
                                ->maxAgeInMinutes(26)
                                ->build()
                        )
                        ->build()
                )
                ->build(),
            QueryExecutionBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->query('Query0')
                ->statementType(StatementType1Enum::UTILITY)
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
                ->resultReuseConfiguration(
                    ResultReuseConfiguration1Builder::init()
                        ->resultReuseByAgeConfiguration(
                            ResultReuseByAgeConfiguration2Builder::init(
                                false
                            )
                                ->maxAgeInMinutes(26)
                                ->build()
                        )
                        ->build()
                )
                ->build()
        ]
    )
    ->unprocessedQueryExecutionIds(
        [
            UnprocessedQueryExecutionIdBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->build(),
            UnprocessedQueryExecutionIdBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->build(),
            UnprocessedQueryExecutionIdBuilder::init()
                ->queryExecutionId('QueryExecutionId6')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->build()
        ]
    )
    ->build();
```



