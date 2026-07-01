# Apply to Resources Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkFwcGx5VG9SZXNvdXJjZXNSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`ApplyToResourcesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `applyTo` | [`FirewallApplyToResources[]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/firewall-apply-to-resources.md) | Required | Resources the Firewall should be applied to | getApplyTo(): array | setApplyTo(array applyTo): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ApplyToResourcesRequestBuilder;
use HetznerCloudApiLib\Models\Builders\FirewallApplyToResourcesBuilder;
use HetznerCloudApiLib\Models\Builders\LabelSelector5Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Server9Builder;
use HetznerCloudApiLib\Models\Type7;

$applyToResourcesRequest = ApplyToResourcesRequestBuilder::init(
    [
        FirewallApplyToResourcesBuilder::init()
            ->labelSelector(
                LabelSelector5Builder::init(
                    'selector8'
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->server(
                Server9Builder::init(
                    14
                )
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            )
            ->type(Type7::SERVER)
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    ]
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



