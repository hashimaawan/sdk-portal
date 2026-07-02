# Tag Resource Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlRhZ1Jlc291cmNlSW5wdXQ


# Class Name

`TagResourceInput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `resourceARN` | `string` | Required | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1011` | getResourceARN(): string | setResourceARN(string resourceARN): void |
| `tags` | [`Tag[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/tag.md) | Required | - | getTags(): array | setTags(array tags): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\TagResourceInputBuilder;
use AmazonAthenaLib\Models\Builders\TagBuilder;

$tagResourceInput = TagResourceInputBuilder::init(
    'ResourceARN6',
    [
        TagBuilder::init()
            ->key('Key0')
            ->value('Value6')
            ->build()
    ]
)->build();
```



