# List Work Groups Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzSW5wdXQ


# Class Name

`ListWorkGroupsInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |
| `maxResults` | `?int` | Optional | **Constraints**: `>= 1`, `<= 50` | getMaxResults(): ?int | setMaxResults(?int maxResults): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListWorkGroupsInputBuilder;

$listWorkGroupsInput = ListWorkGroupsInputBuilder::init()
    ->nextToken('NextToken8')
    ->maxResults(50)
    ->build();
```



