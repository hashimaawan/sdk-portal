# Batch Get Prepared Statement Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0UHJlcGFyZWRTdGF0ZW1lbnRPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`BatchGetPreparedStatementOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `preparedStatements` | [`?(PreparedStatement[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/prepared-statement.md) | Optional | - | getPreparedStatements(): ?array | setPreparedStatements(?array preparedStatements): void |
| `unprocessedPreparedStatementNames` | [`?(UnprocessedPreparedStatementName[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/unprocessed-prepared-statement-name.md) | Optional | - | getUnprocessedPreparedStatementNames(): ?array | setUnprocessedPreparedStatementNames(?array unprocessedPreparedStatementNames): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetPreparedStatementOutputBuilder;
use AmazonAthenaLib\Models\Builders\PreparedStatementBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\UnprocessedPreparedStatementNameBuilder;

$batchGetPreparedStatementOutput = BatchGetPreparedStatementOutputBuilder::init()
    ->preparedStatements(
        [
            PreparedStatementBuilder::init()
                ->statementName('StatementName2')
                ->queryStatement('QueryStatement6')
                ->workGroupName('WorkGroupName6')
                ->description('Description2')
                ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            PreparedStatementBuilder::init()
                ->statementName('StatementName2')
                ->queryStatement('QueryStatement6')
                ->workGroupName('WorkGroupName6')
                ->description('Description2')
                ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->unprocessedPreparedStatementNames(
        [
            UnprocessedPreparedStatementNameBuilder::init()
                ->statementName('StatementName0')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            UnprocessedPreparedStatementNameBuilder::init()
                ->statementName('StatementName0')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            UnprocessedPreparedStatementNameBuilder::init()
                ->statementName('StatementName0')
                ->errorCode('ErrorCode2')
                ->errorMessage('ErrorMessage8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



