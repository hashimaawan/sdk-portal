# Calculation Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNhbGN1bGF0aW9uQ29uZmlndXJhdGlvbg

Contains configuration information for the calculation.

*This model accepts additional fields of type array.*


# Class Name

`CalculationConfiguration`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `codeBlock` | `?string` | Optional | **Constraints**: *Maximum Length*: `68000` | getCodeBlock(): ?string | setCodeBlock(?string codeBlock): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CalculationConfigurationBuilder;
use AmazonAthenaLib\ApiHelper;

$calculationConfiguration = CalculationConfigurationBuilder::init()
    ->codeBlock('CodeBlock2')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



