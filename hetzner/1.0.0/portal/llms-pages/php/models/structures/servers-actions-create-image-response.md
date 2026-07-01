# Servers Actions Create Image Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENyZWF0ZSUyNTIwSW1hZ2UlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsCreateImageResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `action` | [`?Action`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/action.md) | Optional | - | getAction(): ?Action | setAction(?Action action): void |
| `image` | [`?Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/image.md) | Optional | - | getImage(): ?Image | setImage(?Image image): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsCreateImageResponseBuilder;
use HetznerCloudApiLib\Models\Builders\ActionBuilder;
use HetznerCloudApiLib\Models\Builders\Resource2Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Status;
use HetznerCloudApiLib\Models\Builders\ErrorBuilder;
use HetznerCloudApiLib\Models\Builders\ImageBuilder;
use HetznerCloudApiLib\Models\OsFlavor;
use HetznerCloudApiLib\Models\Builders\ProtectionBuilder;
use HetznerCloudApiLib\Models\Status24;
use HetznerCloudApiLib\Models\Type22;
use HetznerCloudApiLib\Models\Builders\CreatedFromBuilder;

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
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                Resource2Builder::init(
                    198,
                    'type0'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ],
            'started8',
            Status::RUNNING
        )
            ->error(
                ErrorBuilder::init(
                    'code2',
                    'message4'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->finished('finished0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
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
            OsFlavor::DEBIAN,
            ProtectionBuilder::init(
                false
            )
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build(),
            Status24::UNAVAILABLE,
            Type22::APP
        )
            ->boundTo(186)
            ->createdFrom(
                CreatedFromBuilder::init(
                    60,
                    'name6'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->deleted('deleted4')
            ->deprecated('deprecated8')
            ->imageSize(141.34)
            ->name('name6')
            ->osVersion('os_version4')
            ->rapidDeploy(false)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



