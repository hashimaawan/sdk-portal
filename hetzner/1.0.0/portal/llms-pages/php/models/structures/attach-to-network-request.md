# Attach to Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkF0dGFjaFRvTmV0d29ya1JlcXVlc3Q

*This model accepts additional fields of type array.*


# Class Name

`AttachToNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `aliasIps` | `?(string[])` | Optional | Additional IPs to be assigned to this Server | getAliasIps(): ?array | setAliasIps(?array aliasIps): void |
| `ip` | `?string` | Optional | IP to request to be assigned to this Server; if you do not provide this then you will be auto assigned an IP address | getIp(): ?string | setIp(?string ip): void |
| `network` | `int` | Required | ID of an existing network to attach the Server to | getNetwork(): int | setNetwork(int network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\AttachToNetworkRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$attachToNetworkRequest = AttachToNetworkRequestBuilder::init(
    4711
)
    ->aliasIps(
        [
            '10.0.1.2'
        ]
    )
    ->ip('10.0.1.1')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



