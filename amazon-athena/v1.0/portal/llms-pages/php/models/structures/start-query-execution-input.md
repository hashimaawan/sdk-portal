# Start Query Execution Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0UXVlcnlFeGVjdXRpb25JbnB1dA


# Class Name

`StartQueryExecutionInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `queryString` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `262144` | getQueryString(): string | setQueryString(string queryString): void |
| `clientRequestToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` | getClientRequestToken(): ?string | setClientRequestToken(?string clientRequestToken): void |
| `queryExecutionContext` | [`?QueryExecutionContext1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-execution-context-1.md) | Optional | - | getQueryExecutionContext(): ?QueryExecutionContext1 | setQueryExecutionContext(?QueryExecutionContext1 queryExecutionContext): void |
| `resultConfiguration` | [`?ResultConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-configuration-1.md) | Optional | - | getResultConfiguration(): ?ResultConfiguration1 | setResultConfiguration(?ResultConfiguration1 resultConfiguration): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `executionParameters` | `?(string[])` | Optional | **Constraints**: *Minimum Items*: `1`, *Minimum Length*: `1`, *Maximum Length*: `1024` | getExecutionParameters(): ?array | setExecutionParameters(?array executionParameters): void |
| `resultReuseConfiguration` | [`?ResultReuseConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-reuse-configuration-1.md) | Optional | - | getResultReuseConfiguration(): ?ResultReuseConfiguration1 | setResultReuseConfiguration(?ResultReuseConfiguration1 resultReuseConfiguration): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartQueryExecutionInputBuilder;
use AmazonAthenaLib\Models\Builders\QueryExecutionContext1Builder;
use AmazonAthenaLib\Models\Builders\ResultConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\EncryptionConfiguration2Builder;
use AmazonAthenaLib\Models\EncryptionOption1Enum;
use AmazonAthenaLib\Models\Builders\AclConfiguration1Builder;
use AmazonAthenaLib\Models\S3AclOption1Enum;

$startQueryExecutionInput = StartQueryExecutionInputBuilder::init(
    'QueryString4'
)
    ->clientRequestToken('ClientRequestToken6')
    ->queryExecutionContext(
        QueryExecutionContext1Builder::init()
            ->database('Database4')
            ->catalog('Catalog0')
            ->build()
    )
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
    ->workGroup('WorkGroup4')
    ->executionParameters(
        [
            'ExecutionParameters8'
        ]
    )
    ->build();
```



