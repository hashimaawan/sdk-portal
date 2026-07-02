# Session Status

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlNlc3Npb25TdGF0dXM

Contains information about the status of a session.


# Class Name

`SessionStatus`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `startDateTime` | `?DateTime` | Optional | - | getStartDateTime(): ?\DateTime | setStartDateTime(?\DateTime startDateTime): void |
| `lastModifiedDateTime` | `?DateTime` | Optional | - | getLastModifiedDateTime(): ?\DateTime | setLastModifiedDateTime(?\DateTime lastModifiedDateTime): void |
| `endDateTime` | `?DateTime` | Optional | - | getEndDateTime(): ?\DateTime | setEndDateTime(?\DateTime endDateTime): void |
| `idleSinceDateTime` | `?DateTime` | Optional | - | getIdleSinceDateTime(): ?\DateTime | setIdleSinceDateTime(?\DateTime idleSinceDateTime): void |
| `state` | [`?string(SessionState1Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/session-state-1.md) | Optional | - | getState(): ?string | setState(?string state): void |
| `stateChangeReason` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getStateChangeReason(): ?string | setStateChangeReason(?string stateChangeReason): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\SessionStatusBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\SessionState1Enum;

$sessionStatus = SessionStatusBuilder::init()
    ->startDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->lastModifiedDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->endDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->idleSinceDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->state(SessionState1Enum::IDLE)
    ->build();
```



