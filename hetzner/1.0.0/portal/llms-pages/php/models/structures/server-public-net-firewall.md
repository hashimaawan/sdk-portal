# Server Public Net Firewall

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlclB1YmxpY05ldEZpcmV3YWxs

*This model accepts additional fields of type array.*


# Class Name

`ServerPublicNetFirewall`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `id` | `?int` | Optional | ID of the Resource | getId(): ?int | setId(?int id): void |
| `status` | [`?string(Status72)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/status-72.md) | Optional | Status of the Firewall on the Server | getStatus(): ?string | setStatus(?string status): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServerPublicNetFirewallBuilder;
use HetznerCloudApiLib\Models\Status72;
use HetznerCloudApiLib\ApiHelper;

$serverPublicNetFirewall = ServerPublicNetFirewallBuilder::init()
    ->id(42)
    ->status(Status72::APPLIED)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



