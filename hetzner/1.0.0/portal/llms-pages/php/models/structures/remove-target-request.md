# Remove Target Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlJlbW92ZVRhcmdldFJlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`RemoveTargetRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `ip` | [`?Ip`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/ip.md) | Optional | IP targets where the traffic should be routed through. It is only possible to use the (Public or vSwitch) IPs of Hetzner Online Root Servers belonging to the project owner. IPs belonging to other users are blocked. Additionally IPs belonging to services provided by Hetzner Cloud (Servers, Load Balancers, ...) are blocked as well. | getIp(): ?Ip | setIp(?Ip ip): void |
| `labelSelector` | [`?LabelSelector12`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/label-selector-12.md) | Optional | Configuration for label selector targets, required if type is `label_selector` | getLabelSelector(): ?LabelSelector12 | setLabelSelector(?LabelSelector12 labelSelector): void |
| `server` | [`?Server16`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/structures/server-16.md) | Optional | Configuration for type Server, required if type is `server` | getServer(): ?Server16 | setServer(?Server16 server): void |
| `type` | [`string(Type29)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/type-29.md) | Required | Type of the resource | getType(): string | setType(string type): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\RemoveTargetRequestBuilder;
use HetznerCloudApiLib\Models\Type29;
use HetznerCloudApiLib\Models\Builders\IpBuilder;
use HetznerCloudApiLib\ApiHelper;
use HetznerCloudApiLib\Models\Builders\LabelSelector12Builder;
use HetznerCloudApiLib\Models\Builders\Server16Builder;

$removeTargetRequest = RemoveTargetRequestBuilder::init(
    Type29::IP
)
    ->ip(
        IpBuilder::init(
            'ip8'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->labelSelector(
        LabelSelector12Builder::init(
            'selector8'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->server(
        Server16Builder::init(
            217.74
        )->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



