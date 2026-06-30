# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/php/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `image` | `string` | Required | ID or name of Image to rebuilt from. | getImage(): string | setImage(string image): void |


# Example

```php
use HetznerCloudAPILib\Models\Builders\RebuildServerRequestBuilder;

$rebuildServerRequest = RebuildServerRequestBuilder::init(
    'ubuntu-20.04'
)->build();
```



