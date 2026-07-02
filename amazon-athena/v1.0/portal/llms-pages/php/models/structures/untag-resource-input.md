# Untag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlVudGFnUmVzb3VyY2VJbnB1dA


# Class Name

`UntagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | getResourceARN(): string | setResourceARN(string resourceARN): void |
| `tagKeys` | `string[]` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` | getTagKeys(): array | setTagKeys(array tagKeys): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\UntagResourceInputBuilder;

$untagResourceInput = UntagResourceInputBuilder::init(
    'ResourceARN6',
    [
        'TagKeys1',
        'TagKeys2',
        'TagKeys3'
    ]
)->build();
```



