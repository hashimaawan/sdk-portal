# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `codeBlock` | `?string` | Optional | **Constraints**: *Maximum Length*: `68000` | getCodeBlock(): ?string | setCodeBlock(?string codeBlock): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CalculationConfigurationBuilder;

$calculationConfiguration = CalculationConfigurationBuilder::init()
    ->codeBlock('CodeBlock2')
    ->build();
```



