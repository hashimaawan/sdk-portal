# Get Query Results Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFF1ZXJ5UmVzdWx0c091dHB1dA


# Class Name

`GetQueryResultsOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `updateCount` | `?int` | Optional | - | getUpdateCount(): ?int | setUpdateCount(?int updateCount): void |
| `resultSet` | [`?ResultSet2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-set-2.md) | Optional | - | getResultSet(): ?ResultSet2 | setResultSet(?ResultSet2 resultSet): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetQueryResultsOutputBuilder;
use AmazonAthenaLib\Models\Builders\ResultSet2Builder;
use AmazonAthenaLib\Models\Builders\RowBuilder;
use AmazonAthenaLib\Models\Builders\DatumBuilder;
use AmazonAthenaLib\Models\Builders\ResultSetMetadata2Builder;
use AmazonAthenaLib\Models\Builders\ColumnInfoBuilder;

$getQueryResultsOutput = GetQueryResultsOutputBuilder::init()
    ->updateCount(60)
    ->resultSet(
        ResultSet2Builder::init()
            ->rows(
                [
                    RowBuilder::init()
                        ->data(
                            [
                                DatumBuilder::init()
                                    ->varCharValue('VarCharValue8')
                                    ->build(),
                                DatumBuilder::init()
                                    ->varCharValue('VarCharValue8')
                                    ->build()
                            ]
                        )
                        ->build(),
                    RowBuilder::init()
                        ->data(
                            [
                                DatumBuilder::init()
                                    ->varCharValue('VarCharValue8')
                                    ->build(),
                                DatumBuilder::init()
                                    ->varCharValue('VarCharValue8')
                                    ->build()
                            ]
                        )
                        ->build()
                ]
            )
            ->resultSetMetadata(
                ResultSetMetadata2Builder::init()
                    ->columnInfo(
                        [
                            ColumnInfoBuilder::init(
                                'Name6',
                                'Type6'
                            )
                                ->catalogName('CatalogName0')
                                ->schemaName('SchemaName0')
                                ->tableName('TableName2')
                                ->label('Label4')
                                ->precision(48)
                                ->build()
                        ]
                    )
                    ->build()
            )
            ->build()
    )
    ->nextToken('NextToken0')
    ->build();
```



