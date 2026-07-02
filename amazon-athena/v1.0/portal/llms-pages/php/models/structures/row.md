# Row

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJvdw

The rows that make up a query result table.


# Class Name

`Row`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `data` | [`?(Datum[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/datum.md) | Optional | - | getData(): ?array | setData(?array data): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\RowBuilder;
use AmazonAthenaLib\Models\Builders\DatumBuilder;

$row = RowBuilder::init()
    ->data(
        [
            DatumBuilder::init()
                ->varCharValue('VarCharValue8')
                ->build()
        ]
    )
    ->build();
```



