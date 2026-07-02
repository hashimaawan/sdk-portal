# Delete Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkRlbGV0ZU5hbWVkUXVlcnlJbnB1dA


# Class Name

`DeleteNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryId` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryId(): string | setNamedQueryId(string namedQueryId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\DeleteNamedQueryInputBuilder;

$deleteNamedQueryInput = DeleteNamedQueryInputBuilder::init(
    'NamedQueryId4'
)->build();
```



