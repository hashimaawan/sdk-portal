# List Sessions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1Jlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`ListSessionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Maximum Length*: `2048` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `sessions` | [`?(SessionSummary[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/session-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `100` | getSessions(): ?array | setSessions(?array sessions): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListSessionsResponseBuilder;
use AmazonAthenaLib\Models\Builders\SessionSummaryBuilder;
use AmazonAthenaLib\Models\Builders\EngineVersion1Builder;
use AmazonAthenaLib\ApiHelper;
use AmazonAthenaLib\Models\Builders\Status3Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\SessionState1;

$listSessionsResponse = ListSessionsResponseBuilder::init()
    ->nextToken('NextToken6')
    ->sessions(
        [
            SessionSummaryBuilder::init()
                ->sessionId('SessionId6')
                ->description('Description4')
                ->engineVersion(
                    EngineVersion1Builder::init()
                        ->selectedEngineVersion('SelectedEngineVersion4')
                        ->effectiveEngineVersion('EffectiveEngineVersion6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->notebookVersion('NotebookVersion6')
                ->status(
                    Status3Builder::init()
                        ->startDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->lastModifiedDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->endDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->idleSinceDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->state(SessionState1::TERMINATING)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            SessionSummaryBuilder::init()
                ->sessionId('SessionId6')
                ->description('Description4')
                ->engineVersion(
                    EngineVersion1Builder::init()
                        ->selectedEngineVersion('SelectedEngineVersion4')
                        ->effectiveEngineVersion('EffectiveEngineVersion6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->notebookVersion('NotebookVersion6')
                ->status(
                    Status3Builder::init()
                        ->startDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->lastModifiedDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->endDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->idleSinceDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->state(SessionState1::TERMINATING)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            SessionSummaryBuilder::init()
                ->sessionId('SessionId6')
                ->description('Description4')
                ->engineVersion(
                    EngineVersion1Builder::init()
                        ->selectedEngineVersion('SelectedEngineVersion4')
                        ->effectiveEngineVersion('EffectiveEngineVersion6')
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->notebookVersion('NotebookVersion6')
                ->status(
                    Status3Builder::init()
                        ->startDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->lastModifiedDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->endDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->idleSinceDateTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
                        ->state(SessionState1::TERMINATING)
                        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                        ->build()
                )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



