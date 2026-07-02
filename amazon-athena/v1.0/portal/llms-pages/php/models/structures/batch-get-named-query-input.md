# Batch Get Named Query Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkJhdGNoR2V0TmFtZWRRdWVyeUlucHV0

Contains an array of named query IDs.


# Class Name

`BatchGetNamedQueryInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `namedQueryIds` | `string[]` | Required | **Constraints**: *Minimum Items*: `1`, *Maximum Items*: `50`, *Minimum Length*: `1`, *Maximum Length*: `128`, *Pattern*: `\S+` | getNamedQueryIds(): array | setNamedQueryIds(array namedQueryIds): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\BatchGetNamedQueryInputBuilder;

$batchGetNamedQueryInput = BatchGetNamedQueryInputBuilder::init(
    [
        'NamedQueryIds3',
        'NamedQueryIds4'
    ]
)->build();
```



