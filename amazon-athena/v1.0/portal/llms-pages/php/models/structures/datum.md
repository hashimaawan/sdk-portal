# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `varCharValue` | `?string` | Optional | - | getVarCharValue(): ?string | setVarCharValue(?string varCharValue): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DatumBuilder;

$datum = DatumBuilder::init()
    ->varCharValue('VarCharValue8')
    ->build();
```



