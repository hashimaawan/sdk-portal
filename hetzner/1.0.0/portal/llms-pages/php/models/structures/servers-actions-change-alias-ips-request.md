# Servers Actions Change Alias Ips Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlNlcnZlcnMlMjUyMEFjdGlvbnMlMjUyMENoYW5nZSUyNTIwQWxpYXMlMjUyMElwcyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`ServersActionsChangeAliasIpsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `aliasIps` | `string[]` | Required | New alias IPs to set for this Server | getAliasIps(): array | setAliasIps(array aliasIps): void |
| `network` | `int` | Required | ID of an existing Network already attached to the Server | getNetwork(): int | setNetwork(int network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\ServersActionsChangeAliasIpsRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$serversActionsChangeAliasIpsRequest = ServersActionsChangeAliasIpsRequestBuilder::init(
    [
        '10.0.1.2'
    ],
    4711
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



