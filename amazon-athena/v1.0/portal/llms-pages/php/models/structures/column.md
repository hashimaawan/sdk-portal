# Column

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNvbHVtbg

Contains metadata for a column in a table.

*This model accepts additional fields of type array.*


# Class Name

`Column`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getName(): string | setName(string name): void |
| `type` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `4096` | getType(): ?string | setType(?string type): void |
| `comment` | `?string` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `255` | getComment(): ?string | setComment(?string comment): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ColumnBuilder;
use AmazonAthenaLib\ApiHelper;

$column = ColumnBuilder::init(
    'Name6'
)
    ->type('Type6')
    ->comment('Comment2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



