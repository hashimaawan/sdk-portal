# Get Calculation Execution Code Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldENhbGN1bGF0aW9uRXhlY3V0aW9uQ29kZVJlc3BvbnNl


# Class Name

`GetCalculationExecutionCodeResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `codeBlock` | `?string` | Optional | **Constraints**: *Maximum Length*: `68000` | getCodeBlock(): ?string | setCodeBlock(?string codeBlock): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetCalculationExecutionCodeResponseBuilder;

$getCalculationExecutionCodeResponse = GetCalculationExecutionCodeResponseBuilder::init()
    ->codeBlock('CodeBlock4')
    ->build();
```



