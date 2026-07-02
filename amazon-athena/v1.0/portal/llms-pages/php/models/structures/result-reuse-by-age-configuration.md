# Result Reuse by Age Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9u

Specifies whether previous query results are reused, and if so, their maximum age.


# Class Name

`ResultReuseByAgeConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `bool` | Required | - | getEnabled(): bool | setEnabled(bool enabled): void |
| `maxAgeInMinutes` | `?int` | Optional | **Constraints**: `>= 0`, `<= 10080` | getMaxAgeInMinutes(): ?int | setMaxAgeInMinutes(?int maxAgeInMinutes): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfigurationBuilder;

$resultReuseByAgeConfiguration = ResultReuseByAgeConfigurationBuilder::init(
    false
)
    ->maxAgeInMinutes(134)
    ->build();
```



