# List Databases Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3REYXRhYmFzZXNJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`ListDatabasesInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `catalogName` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `256` | getCatalogName(): string | setCatalogName(string catalogName): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListDatabasesInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listDatabasesInput = ListDatabasesInputBuilder::init(
    'CatalogName4'
)
    ->nextToken('NextToken0')
    ->maxResults(50)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



