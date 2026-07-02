# Result Reuse by Age Configuration 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQnlBZ2VDb25maWd1cmF0aW9uMg


# Class Name

`ResultReuseByAgeConfiguration2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `enabled` | `bool` | Required | - | getEnabled(): bool | setEnabled(bool enabled): void |
| `maxAgeInMinutes` | `?int` | Optional | **Constraints**: `>= 0`, `<= 10080` | getMaxAgeInMinutes(): ?int | setMaxAgeInMinutes(?int maxAgeInMinutes): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfiguration2Builder;

$resultReuseByAgeConfiguration2 = ResultReuseByAgeConfiguration2Builder::init(
    false
)
    ->maxAgeInMinutes(44)
    ->build();
```



