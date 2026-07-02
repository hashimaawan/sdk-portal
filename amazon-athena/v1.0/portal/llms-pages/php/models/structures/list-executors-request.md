# List Executors Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RFeGVjdXRvcnNSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ListExecutorsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `sessionId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getSessionId(): string | setSessionId(string sessionId): void |
| `executorStateFilter` | [`?string(ExecutorState1)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/executor-state-1.md) | Optional | - | getExecutorStateFilter(): ?string | setExecutorStateFilter(?string executorStateFilter): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 100` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Maximum Length*: `2048` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListExecutorsRequestBuilder;
use AmazonAthenaLib\Models\ExecutorState1;
use AmazonAthenaLib\ApiHelper;

$listExecutorsRequest = ListExecutorsRequestBuilder::init(
    'SessionId0'
)
    ->executorStateFilter(ExecutorState1::CREATING)
    ->maxResults(100)
    ->nextToken('NextToken8')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



