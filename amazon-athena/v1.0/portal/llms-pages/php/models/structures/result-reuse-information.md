# Result Reuse Information

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24

Contains information about whether the result of a previous query was reused.


# Class Name

`ResultReuseInformation`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reusedPreviousResult` | `bool` | Required | - | getReusedPreviousResult(): bool | setReusedPreviousResult(bool reusedPreviousResult): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultReuseInformationBuilder;

$resultReuseInformation = ResultReuseInformationBuilder::init(
    false
)->build();
```



