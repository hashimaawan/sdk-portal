# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA

*This model accepts additional fields of type array.*


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `network` | `int` | Required | ID of an existing network to detach the Server from | getNetwork(): int | setNetwork(int network): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\DetachFromNetworkRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$detachFromNetworkRequest = DetachFromNetworkRequestBuilder::init(
    4711
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



