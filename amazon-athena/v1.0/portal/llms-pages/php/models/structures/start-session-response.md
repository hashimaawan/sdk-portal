# Start Session Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlc3BvbnNl


# Class Name

`StartSessionResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `state` | [`?string(SessionState1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/session-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\StartSessionResponseBuilder;
use AmazonAthenaLib\Models\SessionState1Enum;

$startSessionResponse = StartSessionResponseBuilder::init()
    ->sessionId('SessionId4')
    ->state(SessionState1Enum::CREATING)
    ->build();
```



