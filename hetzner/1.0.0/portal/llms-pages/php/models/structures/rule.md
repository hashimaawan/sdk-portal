# Rule

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlJ1bGU

*This model accepts additional fields of type array.*


# Class Name

`Rule`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `description` | `?string` | Optional | Description of the Rule<br><br>**Constraints**: *Maximum Length*: `255` | getDescription(): ?string | setDescription(?string description): void |
| `destinationIps` | `?(string[])` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. | getDestinationIps(): ?array | setDestinationIps(?array destinationIps): void |
| `direction` | [`string(Direction)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/direction.md) | Required | Select traffic direction on which rule should be applied. Use `source_ips` for direction `in` and `destination_ips` for direction `out`. | getDirection(): string | setDirection(string direction): void |
| `port` | `?string` | Optional | Port or port range to which traffic will be allowed, only applicable for protocols TCP and UDP. A port range can be specified by separating two ports with a dash, e.g `1024-5000`. | getPort(): ?string | setPort(?string port): void |
| `protocol` | [`string(Protocol)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/php/models/enumerations/protocol.md) | Required | Type of traffic to allow | getProtocol(): string | setProtocol(string protocol): void |
| `sourceIps` | `?(string[])` | Optional | List of permitted IPv4/IPv6 addresses in CIDR notation. Use `0.0.0.0/0` to allow all IPv4 addresses and `::/0` to allow all IPv6 addresses. You can specify 100 CIDRs at most. | getSourceIps(): ?array | setSourceIps(?array sourceIps): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\RuleBuilder;
use HetznerCloudApiLib\Models\Direction;
use HetznerCloudApiLib\Models\Protocol;
use HetznerCloudApiLib\ApiHelper;

$rule = RuleBuilder::init(
    Direction::IN,
    Protocol::ESP
)
    ->description('description0')
    ->destinationIps(
        [
            '28.239.13.1/32',
            '28.239.14.0/24',
            'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
        ]
    )
    ->port('80')
    ->sourceIps(
        [
            '28.239.13.1/32',
            '28.239.14.0/24',
            'ff21:1eac:9a3b:ee58:5ca:990c:8bc9:c03b/128'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



