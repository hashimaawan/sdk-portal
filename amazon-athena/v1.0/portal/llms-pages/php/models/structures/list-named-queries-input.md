# List Named Queries Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`ListNamedQueriesInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 0`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNamedQueriesInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listNamedQueriesInput = ListNamedQueriesInputBuilder::init()
    ->nextToken('NextToken8')
    ->maxResults(50)
    ->workGroup('WorkGroup0')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



