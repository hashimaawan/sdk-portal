# List Prepared Statements Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RQcmVwYXJlZFN0YXRlbWVudHNPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`ListPreparedStatementsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `preparedStatements` | [`?(PreparedStatementSummary[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/prepared-statement-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` | getPreparedStatements(): ?array | setPreparedStatements(?array preparedStatements): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListPreparedStatementsOutputBuilder;
use AmazonAthenaLib\Models\Builders\PreparedStatementSummaryBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\ApiHelper;

$listPreparedStatementsOutput = ListPreparedStatementsOutputBuilder::init()
    ->preparedStatements(
        [
            PreparedStatementSummaryBuilder::init()
                ->statementName('StatementName2')
                ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            PreparedStatementSummaryBuilder::init()
                ->statementName('StatementName2')
                ->lastModifiedTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->nextToken('NextToken2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



