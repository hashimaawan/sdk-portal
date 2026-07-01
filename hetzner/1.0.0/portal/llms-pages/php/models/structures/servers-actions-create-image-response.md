# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `image` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getImage(): ?Image | setImage(?Image image): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ServersActionsCreateImageResponseBuilder;
use HetznerCloudAPILib\Models\Builders\ActionBuilder;
use HetznerCloudAPILib\Models\Builders\Resource2Builder;
use HetznerCloudAPILib\Models\StatusEnum;
use HetznerCloudAPILib\Models\Builders\ErrorBuilder;
use HetznerCloudAPILib\Models\Builders\ImageBuilder;
use HetznerCloudAPILib\Models\OsFlavorEnum;
use HetznerCloudAPILib\Models\Builders\ProtectionBuilder;
use HetznerCloudAPILib\Models\Status24Enum;
use HetznerCloudAPILib\Models\Type22Enum;
use HetznerCloudAPILib\Models\Builders\CreatedFromBuilder;

$serversActionsCreateImageResponse = ServersActionsCreateImageResponseBuilder::init()
    ->action(
        ActionBuilder::init(
            'command6',
            238,
            143.26,
            [
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )->build()
            ],
            'started8',
            StatusEnum::RUNNING
        )
            ->error(
                ErrorBuilder::init(
                    'code2',
                    'message4'
                )->build()
            )
            ->finished('finished0')
            ->build()
    )
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



