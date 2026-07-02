# List Databases Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNPdXRwdXQ

*This model accepts additional fields of type array.*


# Class Name

`ListDatabasesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `databaseList` | [`?(Database[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/database.md) | Optional | - | getDatabaseList(): ?array | setDatabaseList(?array databaseList): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListDatabasesOutputBuilder;
use AmazonAthenaLib\Models\Builders\DatabaseBuilder;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;
use AmazonAthenaLib\ApiHelper;

$listDatabasesOutput = ListDatabasesOutputBuilder::init()
    ->databaseList(
        [
            DatabaseBuilder::init(
                'Name4'
            )
                ->description('Description8')
                ->parameters(
                    ParametersBuilder::init()
                        ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DatabaseBuilder::init(
                'Name4'
            )
                ->description('Description8')
                ->parameters(
                    ParametersBuilder::init()
                        ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            DatabaseBuilder::init(
                'Name4'
            )
                ->description('Description8')
                ->parameters(
                    ParametersBuilder::init()
                        ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->nextToken('NextToken6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



