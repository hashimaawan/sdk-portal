# Firewall Remove from Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsUmVtb3ZlRnJvbVJlc291cmNlcw


# Class Name

`FirewallRemoveFromResources`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelSelector` | [`?LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` | getLabelSelector(): ?LabelSelector5 | setLabelSelector(?LabelSelector5 labelSelector): void |
| `server` | [`?Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` | getServer(): ?Server9 | setServer(?Server9 server): void |
| `type` | [`?string(Type7Enum)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/enumerations/type-7.md) | Optional | Type of the resource | getType(): ?string | setType(?string type): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\FirewallRemoveFromResourcesBuilder;
use HetznerCloudAPILib\Models\Builders\LabelSelector5Builder;
use HetznerCloudAPILib\Models\Builders\Server9Builder;
use HetznerCloudAPILib\Models\Type7Enum;

$firewallRemoveFromResources = FirewallRemoveFromResourcesBuilder::init()
    ->labelSelector(
        LabelSelector5Builder::init(
            'selector8'
        )->build()
    )
    ->server(
        Server9Builder::init(
            14
        )->build()
    )
    ->type(Type7Enum::SERVER)
    ->build();
```



