# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).

*This model accepts additional fields of type array.*


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `varCharValue` | `?string` | Optional | - | getVarCharValue(): ?string | setVarCharValue(?string varCharValue): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DatumBuilder;
use AmazonAthenaLib\ApiHelper;

$datum = DatumBuilder::init()
    ->varCharValue('VarCharValue8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



