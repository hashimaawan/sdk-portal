# Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlNlc3Npb25TdW1tYXJ5

Contains summary information about a session.


# Class Name

`SessionSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `description` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getDescription(): ?string | setDescription(?string description): void |
| `engineVersion` | [`?EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/engine-version-1.md) | Optional | - | getEngineVersion(): ?EngineVersion1 | setEngineVersion(?EngineVersion1 engineVersion): void |
| `notebookVersion` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getNotebookVersion(): ?string | setNotebookVersion(?string notebookVersion): void |
| `status` | [`?Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status-3.md) | Optional | - | getStatus(): ?Status3 | setStatus(?Status3 status): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\SessionSummaryBuilder;
use AmazonAthenaLib\Models\Builders\EngineVersion1Builder;
use AmazonAthenaLib\Models\Builders\Status3Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\SessionState1Enum;

$sessionSummary = SessionSummaryBuilder::init()
    ->sessionId('SessionId0')
    ->description('Description8')
    ->engineVersion(
        EngineVersion1Builder::init()
            ->selectedEngineVersion('SelectedEngineVersion4')
            ->effectiveEngineVersion('EffectiveEngineVersion6')
            ->build()
    )
    ->notebookVersion('NotebookVersion2')
    ->status(
        Status3Builder::init()
            ->startDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->lastModifiedDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->endDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->idleSinceDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
            ->state(SessionState1Enum::TERMINATING)
            ->build()
    )
    ->build();
```



