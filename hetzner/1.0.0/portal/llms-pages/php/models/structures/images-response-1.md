# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `image` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getImage(): ?Image | setImage(?Image image): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ImagesResponse1Builder;
use HetznerCloudAPILib\Models\Builders\ImageBuilder;
use HetznerCloudAPILib\Models\OsFlavorEnum;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status24Enum;
use HetznerCloudAPILib\Models\Type22Enum;
use HetznerCloudAPILib\Models\Builders\CreatedFromBuilder;

$imagesResponse1 = ImagesResponse1Builder::init()
    ->image(
        ImageBuilder::init(
            'created6',
            'description6',
            244.18,
            128,
            [
                'key0' => 'labels4'
            ],
            OsFlavorEnum::DEBIAN,
            ProtectionBuilder::init(
                false
            )->build(),
            Status24Enum::UNAVAILABLE,
            Type22Enum::APP
        )
            ->boundTo(186)
            ->createdFrom(
                CreatedFromBuilder::init(
                    60,
                    'name6'
                )->build()
            )
            ->deleted('deleted4')
            ->deprecated('deprecated8')
            ->imageSize(141.34)
            ->name('name6')
            ->osVersion('os_version4')
            ->rapidDeploy(false)
            ->build()
    )
    ->build();
```



