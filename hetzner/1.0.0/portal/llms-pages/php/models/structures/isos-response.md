# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `isos` | [`Iso[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/iso.md) | Required | - | getIsos(): array | setIsos(array isos): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\IsosResponseBuilder;
use HetznerCloudAPILib\Models\Builders\IsoBuilder;
use HetznerCloudAPILib\Models\Type26Enum;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$isosResponse = IsosResponseBuilder::init(
    [
        IsoBuilder::init(
            'FreeBSD 11.0 x64',
            42,
            Type26Enum::PUBLIC_
        )
            ->deprecated('2018-02-28T00:00:00+00:00')
            ->name('FreeBSD-11.0-RELEASE-amd64-dvd1')
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



