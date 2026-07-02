# Result Reuse Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlQ29uZmlndXJhdGlvbjE


# Class Name

`ResultReuseConfiguration1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resultReuseByAgeConfiguration` | [`?ResultReuseByAgeConfiguration2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/result-reuse-by-age-configuration-2.md) | Optional | - | getResultReuseByAgeConfiguration(): ?ResultReuseByAgeConfiguration2 | setResultReuseByAgeConfiguration(?ResultReuseByAgeConfiguration2 resultReuseByAgeConfiguration): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultReuseConfiguration1Builder;
use AmazonAthenaLib\Models\Builders\ResultReuseByAgeConfiguration2Builder;

$resultReuseConfiguration1 = ResultReuseConfiguration1Builder::init()
    ->resultReuseByAgeConfiguration(
        ResultReuseByAgeConfiguration2Builder::init(
            false
        )
            ->maxAgeInMinutes(26)
            ->build()
    )
    ->build();
```



