# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `databaseList` | [`?(Database[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/database.md) | Optional | - | getDatabaseList(): ?array | setDatabaseList(?array databaseList): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListDatabasesOutputBuilder;
use AmazonAthenaLib\Models\Builders\DatabaseBuilder;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;

$listDatabasesOutput = ListDatabasesOutputBuilder::init()
    ->databaseList(
        [
            DatabaseBuilder::init(
                'Name4'
            )
                ->description('Description8')
                ->parameters(
                    ParametersBuilder::init()->build()
                )->build(),
            DatabaseBuilder::init(
                'Name4'
            )
                ->description('Description8')
                ->parameters(
                    ParametersBuilder::init()->build()
                )->build(),
            DatabaseBuilder::init(
                'Name4'
            )
                ->description('Description8')
                ->parameters(
                    ParametersBuilder::init()->build()
                )->build()
        ]
    )
    ->nextToken('NextToken6')
    ->build();
```



