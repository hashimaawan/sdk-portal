# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.

*This model accepts additional fields of type array.*


# Class Name

`Row`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(Datum[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/datum.md) | Optional | - | getData(): ?array | setData(?array data): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\RowBuilder;
use AmazonAthenaLib\Models\Builders\DatumBuilder;
use AmazonAthenaLib\ApiHelper;

$row = RowBuilder::init()
    ->data(
        [
            DatumBuilder::init()
                ->varCharValue('VarCharValue8')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



