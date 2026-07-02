# Create Named Query Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkNyZWF0ZU5hbWVkUXVlcnlPdXRwdXQ


# Class Name

`CreateNamedQueryOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryId` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryId(): ?string | setNamedQueryId(?string namedQueryId): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\CreateNamedQueryOutputBuilder;

$createNamedQueryOutput = CreateNamedQueryOutputBuilder::init()
    ->namedQueryId('NamedQueryId0')
    ->build();
```



