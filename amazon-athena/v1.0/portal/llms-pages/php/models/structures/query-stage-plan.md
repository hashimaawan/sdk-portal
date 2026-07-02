# Query Stage Plan

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFu


# Class Name

`QueryStagePlan`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `identifier` | `?string` | Optional | - | getIdentifier(): ?string | setIdentifier(?string identifier): void |
| `children` | [`?(QueryStagePlanNode[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-stage-plan-node.md) | Optional | - | getChildren(): ?array | setChildren(?array children): void |
| `remoteSources` | `?(string[])` | Optional | - | getRemoteSources(): ?array | setRemoteSources(?array remoteSources): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryStagePlanBuilder;
use AmazonAthenaLib\Models\Builders\QueryStagePlanNodeBuilder;

$queryStagePlan = QueryStagePlanBuilder::init()
    ->name('Name0')
    ->identifier('Identifier6')
    ->children(
        [
            QueryStagePlanNodeBuilder::init()
                ->name('Name6')
                ->identifier('Identifier2')
                ->children(
                    [
                        QueryStagePlanNodeBuilder::init()->build()
                    ]
                )
                ->remoteSources(
                    [
                        'RemoteSources4',
                        'RemoteSources5',
                        'RemoteSources6'
                    ]
                )
                ->build()
        ]
    )
    ->remoteSources(
        [
            'RemoteSources8',
            'RemoteSources9',
            'RemoteSources0'
        ]
    )
    ->build();
```



