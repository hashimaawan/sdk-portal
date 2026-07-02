# Get Database Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldERhdGFiYXNlT3V0cHV0

*This model accepts additional fields of type array.*


# Class Name

`GetDatabaseOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `database` | [`?Database2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/database-2.md) | Optional | - | getDatabase(): ?Database2 | setDatabase(?Database2 database): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetDatabaseOutputBuilder;
use AmazonAthenaLib\Models\Builders\Database2Builder;
use AmazonAthenaLib\Models\Builders\ParametersBuilder;
use AmazonAthenaLib\ApiHelper;

$getDatabaseOutput = GetDatabaseOutputBuilder::init()
    ->database(
        Database2Builder::init(
            'Name2'
        )
            ->description('Description8')
            ->parameters(
                ParametersBuilder::init()
                    ->additionalProperty('exampleAdditionalProperty', 'Parameters_additionalProperties2')
                    ->build()
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



