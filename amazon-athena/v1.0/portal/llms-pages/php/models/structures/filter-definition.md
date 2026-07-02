# Filter Definition

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkZpbHRlckRlZmluaXRpb24

A string for searching notebook names.

*This model accepts additional fields of type array.*


# Class Name

`FilterDefinition`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `255` | getName(): ?string | setName(?string name): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\FilterDefinitionBuilder;
use AmazonAthenaLib\ApiHelper;

$filterDefinition = FilterDefinitionBuilder::init()
    ->name('Name2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



