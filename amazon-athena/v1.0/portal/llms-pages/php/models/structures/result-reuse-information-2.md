# Result Reuse Information 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlJlc3VsdFJldXNlSW5mb3JtYXRpb24y


# Class Name

`ResultReuseInformation2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `reusedPreviousResult` | `bool` | Required | - | getReusedPreviousResult(): bool | setReusedPreviousResult(bool reusedPreviousResult): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ResultReuseInformation2Builder;

$resultReuseInformation2 = ResultReuseInformation2Builder::init(
    false
)->build();
```



