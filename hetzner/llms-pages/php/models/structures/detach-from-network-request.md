# Detach from Network Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRkRldGFjaEZyb21OZXR3b3JrUmVxdWVzdA


# Class Name

`DetachFromNetworkRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `network` | `int` | Required | ID of an existing network to detach the Server from | getNetwork(): int | setNetwork(int network): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\DetachFromNetworkRequestBuilder;

$detachFromNetworkRequest = DetachFromNetworkRequestBuilder::init(
    4711
)->build();
```



