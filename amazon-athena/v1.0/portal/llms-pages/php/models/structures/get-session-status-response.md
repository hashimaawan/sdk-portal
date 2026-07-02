# Get Session Status Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkdldFNlc3Npb25TdGF0dXNSZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`GetSessionStatusResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `status` | [`?Status3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/status-3.md) | Optional | - | getStatus(): ?Status3 | setStatus(?Status3 status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\GetSessionStatusResponseBuilder;
use AmazonAthenaLib\Models\Builders\Status3Builder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\Models\SessionState1;
use AmazonAthenaLib\ApiHelper;

$getSessionStatusResponse = GetSessionStatusResponseBuilder::init()
    ->sessionId('SessionId4')
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
    ->build();
```



