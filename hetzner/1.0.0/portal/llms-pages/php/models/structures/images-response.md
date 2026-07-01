# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `images` | [`Image[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image.md) | Required | - | getImages(): array | setImages(array images): void |
| `meta` | [`?Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/meta.md) | Optional | - | getMeta(): ?Meta | setMeta(?Meta meta): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ImagesResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ImageBuilder;
use HetznerCloudAPILib\Models\OsFlavorEnum;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status24Enum;
use HetznerCloudAPILib\Models\Type22Enum;
use HetznerCloudAPILib\Models\Builders\CreatedFromBuilder;
use HetznerCloudAPILib\Models\Builders\MetaBuilder;
use HetznerCloudAPILib\Models\Builders\PaginationBuilder;

$imagesResponse = ImagesResponseBuilder::init(
    [
        ImageBuilder::init(
            '2016-01-30T23:55:00+00:00',
            'Ubuntu 20.04 Standard 64 bit',
            10,
            42,
            [
                'key0' => 'labels0',
                'key1' => 'labels1'
            ],
            OsFlavorEnum::UBUNTU,
            ProtectionBuilder::init(
                false
            )->build(),
            Status24Enum::AVAILABLE,
            Type22Enum::SNAPSHOT
        )
            ->boundTo(null)
            ->createdFrom(
                CreatedFromBuilder::init(
                    1,
                    'Server'
                )->build()
            )
            ->deleted(null)
            ->deprecated('2018-02-28T00:00:00+00:00')
            ->imageSize(2.3)
            ->name('ubuntu-20.04')
            ->osVersion('20.04')
            ->rapidDeploy(false)
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



