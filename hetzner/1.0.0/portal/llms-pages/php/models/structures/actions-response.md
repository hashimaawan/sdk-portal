# Actions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFjdGlvbnNSZXNwb25zZQ


# Class Name

`ActionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `actions` | [`Action[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Required | - | getActions(): array | setActions(array actions): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ActionsResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$actionsResponse = ActionsResponseBuilder::init(
    [
        ActionBuilder::init(
            'start_server',
            42,
            100,
            [
                Resource2Builder::init(
                    42,
                    'server'
                )->build()
            ],
            '2016-01-30T23:55:00+00:00',
            StatusEnum::SUCCESS
        )
            ->error(
                ErrorBuilder::init(
                    'action_failed',
                    'Action failed'
                )->build()
            )
            ->finished('2016-01-30T23:55:00+00:00')
            ->build()
    ]
)
    ->meta(
        MetaBuilder::init(
            PaginationBuilder::init(
                17.58,
                13.34
            )
                ->lastPage(77.7)
                ->nextPage(209.18)
                ->previousPage(50.02)
                ->totalEntries(206.64)
                ->build()
        )->build()
    )->build();
```



