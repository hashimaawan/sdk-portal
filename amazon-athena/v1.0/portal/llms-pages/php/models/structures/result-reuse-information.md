# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.

*This model accepts additional fields of type array.*


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reusedPreviousResult` | `bool` | Required | - | getReusedPreviousResult(): bool | setReusedPreviousResult(bool reusedPreviousResult): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultReuseInformationBuilder;
use AmazonAthenaLib\ApiHelper;

$resultReuseInformation = ResultReuseInformationBuilder::init(
    false
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



