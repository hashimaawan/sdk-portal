# List Calculation Executions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RDYWxjdWxhdGlvbkV4ZWN1dGlvbnNSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ListCalculationExecutionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |
| `stateFilter` | [`?string(CalculationExecutionState3)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/calculation-execution-state-3.md) | Optional | - | getStateFilter(): ?string | setStateFilter(?string stateFilter): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 100` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Maximum Length*: `2048` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListCalculationExecutionsRequestBuilder;
use AmazonAthenaLib\Models\CalculationExecutionState3;
use AmazonAthenaLib\ApiHelper;

$listCalculationExecutionsRequest = ListCalculationExecutionsRequestBuilder::init(
    'SessionId2'
)
    ->stateFilter(CalculationExecutionState3::QUEUED)
    ->maxResults(100)
    ->nextToken('NextToken0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



