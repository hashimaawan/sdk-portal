# Batch Get Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeU91dHB1dA

*This model accepts additional fields of type array.*


# Class Name

`BatchGetNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueries` | [`?(NamedQuery[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/named-query.md) | Optional | - | getNamedQueries(): ?array | setNamedQueries(?array namedQueries): void |
| `unprocessedNamedQueryIds` | [`?(UnprocessedNamedQueryId[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/unprocessed-named-query-id.md) | Optional | - | getUnprocessedNamedQueryIds(): ?array | setUnprocessedNamedQueryIds(?array unprocessedNamedQueryIds): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetNamedQueryOutputBuilder;
use AmazonAthenaLib\Models\Builders\NamedQueryBuilder;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\UnprocessedNamedQueryIdBuilder;

$batchGetNamedQueryOutput = BatchGetNamedQueryOutputBuilder::init()
    ->namedQueries(
        [
            NamedQueryBuilder::init(
                'Name2',
                'Database0',
                'QueryString4'
            )
                ->description('Description4')
                ->namedQueryId('NamedQueryId0')
                ->workGroup('WorkGroup4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            NamedQueryBuilder::init(
                'Name2',
                'Database0',
                'QueryString4'
            )
                ->description('Description4')
                ->namedQueryId('NamedQueryId0')
                ->workGroup('WorkGroup4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            NamedQueryBuilder::init(
                'Name2',
                'Database0',
                'QueryString4'
            )
                ->description('Description4')
                ->namedQueryId('NamedQueryId0')
                ->workGroup('WorkGroup4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->unprocessedNamedQueryIds(
        [
            UnprocessedNamedQueryIdBuilder::init()
                ->namedQueryId('NamedQueryId4')
                ->errorCode('ErrorCode6')
                ->errorMessage('ErrorMessage4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            UnprocessedNamedQueryIdBuilder::init()
                ->namedQueryId('NamedQueryId4')
                ->errorCode('ErrorCode6')
                ->errorMessage('ErrorMessage4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



