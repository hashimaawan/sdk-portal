# Filters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkZpbHRlcnM

*This model accepts additional fields of type array.*


# Class Name

`Filters`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\FiltersBuilder;
use AmazonAthenaLib\ApiHelper;

$filters = FiltersBuilder::init()
    ->name('Name0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



