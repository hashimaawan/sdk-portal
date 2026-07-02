# Filters

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkZpbHRlcnM


# Class Name

`Filters`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\FiltersBuilder;

$filters = FiltersBuilder::init()
    ->name('Name0')
    ->build();
```



