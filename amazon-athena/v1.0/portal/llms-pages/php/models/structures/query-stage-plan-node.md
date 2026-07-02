# Query Stage Plan Node

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/php/x-redirect/JTI0bSUyRlF1ZXJ5U3RhZ2VQbGFuTm9kZQ

Stage plan information such as name, identifier, sub plans, and remote sources.


# Class Name

`QueryStagePlanNode`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `?string` | Optional | - | getName(): ?string | setName(?string name): void |
| `identifier` | `?string` | Optional | - | getIdentifier(): ?string | setIdentifier(?string identifier): void |
| `children` | [`?(QueryStagePlanNode[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/php/models/structures/query-stage-plan-node.md) | Optional | - | getChildren(): ?array | setChildren(?array children): void |
| `remoteSources` | `?(string[])` | Optional | - | getRemoteSources(): ?array | setRemoteSources(?array remoteSources): void |


# Example

```php
use AmazonAthenaLib\Models\Builders\QueryStagePlanNodeBuilder;

$queryStagePlanNode = QueryStagePlanNodeBuilder::init()
    ->name('Name4')
    ->identifier('Identifier0')
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
            'RemoteSources2',
            'RemoteSources3',
            'RemoteSources4'
        ]
    )
    ->build();
```



