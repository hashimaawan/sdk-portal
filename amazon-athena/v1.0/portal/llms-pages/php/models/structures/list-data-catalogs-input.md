# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA

*This model accepts additional fields of type array.*


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 2`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListDataCatalogsInputBuilder;
use AmazonAthenaLib\ApiHelper;

$listDataCatalogsInput = ListDataCatalogsInputBuilder::init()
    ->nextToken('NextToken8')
    ->maxResults(50)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



