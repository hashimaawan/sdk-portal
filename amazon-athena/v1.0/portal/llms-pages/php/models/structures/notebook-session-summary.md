# Notebook Session Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRk5vdGVib29rU2Vzc2lvblN1bW1hcnk

Contains the notebook session ID and notebook session creation time.

*This model accepts additional fields of type array.*


# Class Name

`NotebookSessionSummary`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): ?string | setSessionId(?string sessionId): void |
| `creationTime` | `?DateTime` | Optional | - | getCreationTime(): ?\DateTime | setCreationTime(?\DateTime creationTime): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\NotebookSessionSummaryBuilder;
use AmazonAthenaLib\Utils\DateTimeHelper;
use AmazonAthenaLib\ApiHelper;

$notebookSessionSummary = NotebookSessionSummaryBuilder::init()
    ->sessionId('SessionId0')
    ->creationTime(DateTimeHelper::fromRfc3339DateTime('2016-03-13T12:52:32.123Z'))
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



