# Applied To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGxpZWRUbw


# Class Name

`AppliedTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `appliedToResources` | [`?(AppliedToResource[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/applied-to-resource.md) | Optional | - | getAppliedToResources(): ?array | setAppliedToResources(?array appliedToResources): void |
| `labelSelector` | [`?LabelSelector`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/label-selector.md) | Optional | - | getLabelSelector(): ?LabelSelector | setLabelSelector(?LabelSelector labelSelector): void |
| `server` | [`?Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server.md) | Optional | - | getServer(): ?Server | setServer(?Server server): void |
| `type` | [`string(Type6Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-6.md) | Required | Type of resource referenced | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AppliedToBuilder;
use HetznerCloudAPILib\Models\Type6Enum;
use HetznerCloudAPILib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudAPILib\Models\Builders\ServerBuilder;
use HetznerCloudAPILib\Models\Type5Enum;
use HetznerCloudAPILib\Models\Builders\LabelSelectorBuilder;

$appliedTo = AppliedToBuilder::init(
    Type6Enum::SERVER
)
    ->appliedToResources(
        [
            AppliedToResourceBuilder::init()
                ->server(
                    ServerBuilder::init(
                        14
                    )->build()
                )
                ->type(Type5Enum::SERVER)
                ->build(),
            AppliedToResourceBuilder::init()
                ->server(
                    ServerBuilder::init(
                        14
                    )->build()
                )
                ->type(Type5Enum::SERVER)
                ->build()
        ]
    )
    ->labelSelector(
        LabelSelectorBuilder::init(
            'selector8'
        )->build()
    )
    ->server(
        ServerBuilder::init(
            14
        )->build()
    )->build();
```



