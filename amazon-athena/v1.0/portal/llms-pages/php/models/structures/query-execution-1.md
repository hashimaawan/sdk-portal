# Query Execution 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5RXhlY3V0aW9uMQ


# Class Name

`QueryExecution1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryExecutionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getQueryExecutionId(): ?string | setQueryExecutionId(?string queryExecutionId): void |
| `query` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | getQuery(): ?string | setQuery(?string query): void |
| `statementType` | [`?string(StatementType1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/statement-type-1.md) | Optional | - | getStatementType(): ?string | setStatementType(?string statementType): void |
| `resultConfiguration` | [`?ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-configuration-1.md) | Optional | - | getResultConfiguration(): ?ResultConfiguration1 | setResultConfiguration(?ResultConfiguration1 resultConfiguration): void |
| `resultReuseConfiguration` | [`?ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-reuse-configuration-1.md) | Optional | - | getResultReuseConfiguration(): ?ResultReuseConfiguration1 | setResultReuseConfiguration(?ResultReuseConfiguration1 resultReuseConfiguration): void |
| `queryExecutionContext` | [`?QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-execution-context-1.md) | Optional | - | getQueryExecutionContext(): ?QueryExecutionContext1 | setQueryExecutionContext(?QueryExecutionContext1 queryExecutionContext): void |
| `status` | [`?Status`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status.md) | Optional | - | getStatus(): ?Status | setStatus(?Status status): void |
| `statistics` | [`?Statistics`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/statistics.md) | Optional | - | getStatistics(): ?Statistics | setStatistics(?Statistics statistics): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `engineVersion` | [`?EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-version-1.md) | Optional | - | getEngineVersion(): ?EngineVersion1 | setEngineVersion(?EngineVersion1 engineVersion): void |
| `executionParameters` | `?(string[])` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` | getExecutionParameters(): ?array | setExecutionParameters(?array executionParameters): void |
| `substatementType` | `?string` | Optional | - | getSubstatementType(): ?string | setSubstatementType(?string substatementType): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryExecution1Builder;
use AmazonAthenaLib\Models\StatementType1Enum;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;
use AmazonAthenaLib\Models\Builders\ResultReuseConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfiguration2Builder;

$queryExecution1 = QueryExecution1Builder::init()
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
    ->build();
```



