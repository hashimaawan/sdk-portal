# List Sessions Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RTZXNzaW9uc1JlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`ListSessionsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `workGroup` | `string` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): string | setWorkGroup(string workGroup): void |
| `stateFilter` | [`?string(SessionState3)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/enumerations/session-state-3.md) | Optional | - | getStateFilter(): ?string | setStateFilter(?string stateFilter): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 100` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Maximum Length*: `2048` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListSessionsRequestBuilder;
use AmazonAthenaLib\Models\SessionState3;
use AmazonAthenaLib\ApiHelper;

$listSessionsRequest = ListSessionsRequestBuilder::init(
    'WorkGroup8'
)
    ->stateFilter(SessionState3::CREATING)
    ->maxResults(100)
    ->nextToken('NextToken6')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



