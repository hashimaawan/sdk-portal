# List Executors Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXNwb25zZQ

*This model accepts additional fields of type array.*


# Class Name

`ListExecutorsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Maximum Length*: `2048` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `executorsSummary` | [`?(ExecutorsSummary[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/executors-summary.md) | Optional | - | getExecutorsSummary(): ?array | setExecutorsSummary(?array executorsSummary): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListExecutorsResponseBuilder;
use AmazonAthenaLib\Models\Builders\ExecutorsSummaryBuilder;
use AmazonAthenaLib\Models\ExecutorType2;
use AmazonAthenaLib\Models\ExecutorState3;
use AmazonAthenaLib\ApiHelper;

$listExecutorsResponse = ListExecutorsResponseBuilder::init(
    'SessionId4'
)
    ->nextToken('NextToken4')
    ->executorsSummary(
        [
            ExecutorsSummaryBuilder::init(
                'ExecutorId8'
            )
                ->executorType(ExecutorType2::GATEWAY)
                ->startDateTime(128)
                ->terminationDateTime(236)
                ->executorState(ExecutorState3::TERMINATED)
                ->executorSize(42)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ExecutorsSummaryBuilder::init(
                'ExecutorId8'
            )
                ->executorType(ExecutorType2::GATEWAY)
                ->startDateTime(128)
                ->terminationDateTime(236)
                ->executorState(ExecutorState3::TERMINATED)
                ->executorSize(42)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            ExecutorsSummaryBuilder::init(
                'ExecutorId8'
            )
                ->executorType(ExecutorType2::GATEWAY)
                ->startDateTime(128)
                ->terminationDateTime(236)
                ->executorState(ExecutorState3::TERMINATED)
                ->executorSize(42)
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



