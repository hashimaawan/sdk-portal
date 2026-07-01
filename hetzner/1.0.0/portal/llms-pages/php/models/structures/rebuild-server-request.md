# Rebuild Server Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/php/x-redirect/JTI0bSUyRlJlYnVpbGRTZXJ2ZXJSZXF1ZXN0

*This model accepts additional fields of type array.*


# Class Name

`RebuildServerRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `image` | `string` | Required | ID or name of Image to rebuilt from. | getImage(): string | setImage(string image): void |
| `additionalProperties` | `array<string, array>` | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use HetznerCloudApiLib\Models\Builders\RebuildServerRequestBuilder;
use HetznerCloudApiLib\ApiHelper;

$rebuildServerRequest = RebuildServerRequestBuilder::init(
    'ubuntu-20.04'
)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



