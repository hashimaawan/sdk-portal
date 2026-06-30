# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRk1ldGE


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/pagination.md) | Required | - | getPagination(): Pagination | setPagination(Pagination pagination): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$meta = MetaBuilder::init(
    PaginationBuilder::init(
        3,
        25
    )
        ->lastPage(4)
        ->nextPage(4)
        ->previousPage(2)
        ->totalEntries(100)
        ->build()
)->build();
```



