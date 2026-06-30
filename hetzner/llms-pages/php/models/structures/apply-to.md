# Apply To

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFwcGx5VG8


# Class Name

`ApplyTo`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelSelector` | [`?LabelSelector1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/label-selector-1.md) | Optional | Configuration for type LabelSelector, required if type is `label_selector` | getLabelSelector(): ?LabelSelector1 | setLabelSelector(?LabelSelector1 labelSelector): void |
| `server` | [`?Server2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-2.md) | Optional | Configuration for type Server, required if type is `server` | getServer(): ?Server2 | setServer(?Server2 server): void |
| `type` | [`string(Type7Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-7.md) | Required | Type of the resource | getType(): string | setType(string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ApplyToBuilder;
use HetznerCloudAPILib\Models\Type7Enum;
use HetznerCloudAPILib\Models\Builders\LabelSelector1Builder;
use HetznerCloudAPILib\Models\Builders\Server2Builder;

$applyTo = ApplyToBuilder::init(
    Type7Enum::SERVER
)
    ->labelSelector(
        LabelSelector1Builder::init(
            'selector8'
        )->build()
    )
    ->server(
        Server2Builder::init(
            14
        )->build()
    )->build();
```



