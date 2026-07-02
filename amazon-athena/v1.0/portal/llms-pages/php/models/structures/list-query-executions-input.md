# List Query Executions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RRdWVyeUV4ZWN1dGlvbnNJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`ListQueryExecutionsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 0`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `workGroup` | `?string` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` | getWorkGroup(): ?string | setWorkGroup(?string workGroup): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListQueryExecutionsInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listQueryExecutionsInput = ListQueryExecutionsInputBuilder::init()
    ->nextToken('NextToken2')
    ->maxResults(34)
    ->workGroup('WorkGroup4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



