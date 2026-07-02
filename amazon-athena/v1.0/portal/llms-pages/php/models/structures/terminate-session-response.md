# Terminate Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlRlcm1pbmF0ZVNlc3Npb25SZXNwb25zZQ


# Class Name

`TerminateSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `state` | [`?string(SessionState1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/session-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\TerminateSessionResponseBuilder;
use AmazonAthenaLib\Models\SessionState1Enum;

$terminateSessionResponse = TerminateSessionResponseBuilder::init()
    ->state(SessionState1Enum::CREATING)
    ->build();
```



