# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.


# Class Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\FilterDefinitionBuilder;

$filterDefinition = FilterDefinitionBuilder::init()
    ->name('Name2')
    ->build();
```



