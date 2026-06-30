# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applyTo` | [`FirewallApplyToResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/php/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to | getApplyTo(): array | setApplyTo(array applyTo): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\ApplyToResourcesRequestBuilder;
use HetznerCloudAPILib\Models\Builders\FirewallApplyToResourcesBuilder;
use HetznerCloudAPILib\Models\Builders\LabelSelector5Builder;
use HetznerCloudAPILib\Models\Builders\Server9Builder;
use HetznerCloudAPILib\Models\Type7Enum;

$applyToResourcesRequest = ApplyToResourcesRequestBuilder::init(
    [
        FirewallApplyToResourcesBuilder::init()
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



