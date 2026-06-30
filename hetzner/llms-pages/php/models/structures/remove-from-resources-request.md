# Remove from Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlJlbW92ZUZyb21SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`RemoveFromResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `removeFrom` | [`FirewallRemoveFromResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/firewall-remove-from-resources.md) | Required | Resources the Firewall should be removed from | getRemoveFrom(): array | setRemoveFrom(array removeFrom): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\RemoveFromResourcesRequestBuilder;
use HetznerCloudAPILib\Models\Builders\FirewallRemoveFromResourcesBuilder;
use HetznerCloudAPILib\Models\Builders\LabelSelector5Builder;
use HetznerCloudAPILib\Models\Builders\Server9Builder;
use HetznerCloudAPILib\Models\Type7Enum;

$removeFromResourcesRequest = RemoveFromResourcesRequestBuilder::init(
    [
        FirewallRemoveFromResourcesBuilder::init()
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
            ->build()
    ]
)->build();
```



