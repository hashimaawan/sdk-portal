# List Tags for Resource Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRkxpc3RUYWdzRm9yUmVzb3VyY2VPdXRwdXQ


# Class Name

`ListTagsForResourceOutput`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `tags` | [`?(Tag[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/tag.md) | Optional | - | getTags(): ?array | setTags(?array tags): void |
| `nextToken` | `?string` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` | getNextToken(): ?string | setNextToken(?string nextToken): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\ListTagsForResourceOutputBuilder;
use AmazonAthenaLib\Models\Builders\TagBuilder;

$listTagsForResourceOutput = ListTagsForResourceOutputBuilder::init()
    ->tags(
        [
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->build(),
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->build(),
            TagBuilder::init()
                ->key('Key0')
                ->value('Value6')
                ->build()
        ]
    )
    ->nextToken('NextToken4')
    ->build();
```



