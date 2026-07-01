# Firewall Apply to Resources

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkZpcmV3YWxsQXBwbHlUb1Jlc291cmNlcw

*This model accepts additional fields of type array.*


# Class Name

`FirewallApplyToResources`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `labelSelector` | [`?LabelSelector5`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/label-selector-5.md) | Optional | Configuration for type label_selector, required if type is `label_selector` | getLabelSelector(): ?LabelSelector5 | setLabelSelector(?LabelSelector5 labelSelector): void |
| `server` | [`?Server9`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-9.md) | Optional | Configuration for type server, required if type is `server` | getServer(): ?Server9 | setServer(?Server9 server): void |
| `type` | [`?string(Type7)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-7.md) | Optional | Type of the resource | getType(): ?string | setType(?string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\FirewallApplyToResourcesBuilder;
use HetznerCloudApiLib\Models\Builders\LabelSelector5Builder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\Server9Builder;
use HetznerCloudApiLib\Models\Type7;

$firewallApplyToResources = FirewallApplyToResourcesBuilder::init()
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
    ->build();
```



