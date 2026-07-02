# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `codeBlock` | `?string` | Optional | **Constraints**: *Maximum Length*: `68000` | getCodeBlock(): ?string | setCodeBlock(?string codeBlock): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetCalculationExecutionCodeResponseBuilder;
use AmazonAthenaLib\ApiHelper;

$getCalculationExecutionCodeResponse = GetCalculationExecutionCodeResponseBuilder::init()
    ->codeBlock('CodeBlock4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



