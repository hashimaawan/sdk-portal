# Applied to Resource

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFwcGxpZWRUb1Jlc291cmNl


# Class Name

`AppliedToResource`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `server` | [`?Server`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server.md) | Optional | - | getServer(): ?Server | setServer(?Server server): void |
| `type` | [`?string(Type5Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-5.md) | Optional | Type of resource referenced | getType(): ?string | setType(?string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\AppliedToResourceBuilder;
use HetznerCloudAPILib\Models\Builders\ServerBuilder;
use HetznerCloudAPILib\Models\Type5Enum;

$appliedToResource = AppliedToResourceBuilder::init()
    ->server(
        ServerBuilder::init(
            14
        )->build()
    )
    ->type(Type5Enum::SERVER)
    ->build();
```



