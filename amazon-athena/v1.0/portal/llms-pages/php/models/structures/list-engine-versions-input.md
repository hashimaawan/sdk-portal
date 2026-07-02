# List Engine Versions Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc0lucHV0


# Class Name

`ListEngineVersionsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 10` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListEngineVersionsInputBuilder;

$listEngineVersionsInput = ListEngineVersionsInputBuilder::init()
    ->nextToken('NextToken6')
    ->maxResults(10)
    ->build();
```



