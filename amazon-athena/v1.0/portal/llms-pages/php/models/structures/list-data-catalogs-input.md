# List Data Catalogs Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3REYXRhQ2F0YWxvZ3NJbnB1dA


# Class Name

`ListDataCatalogsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 2`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListDataCatalogsInputBuilder;

$listDataCatalogsInput = ListDataCatalogsInputBuilder::init()
    ->nextToken('NextToken8')
    ->maxResults(50)
    ->build();
```



