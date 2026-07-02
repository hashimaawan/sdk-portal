# List Named Queries Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3ROYW1lZFF1ZXJpZXNPdXRwdXQ


# Class Name

`ListNamedQueriesOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryIds` | `?(string[])` | Optional | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryIds(): ?array | setNamedQueryIds(?array namedQueryIds): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListNamedQueriesOutputBuilder;

$listNamedQueriesOutput = ListNamedQueriesOutputBuilder::init()
    ->namedQueryIds(
        [
            'NamedQueryIds5',
            'NamedQueryIds4',
            'NamedQueryIds3'
        ]
    )
    ->nextToken('NextToken2')
    ->build();
```



