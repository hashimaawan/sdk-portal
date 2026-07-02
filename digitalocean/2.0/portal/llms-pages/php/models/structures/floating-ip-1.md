# Floating Ip 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkZsb2F0aW5nSXAx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`FloatingIp1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `droplet` | array\|null\|[Droplet](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet.md)\|null | Optional | This is a container for any-of cases. | getDroplet(): | setDroplet( droplet): void |
| `ip` | `?string` | Optional | The public IP address of the floating IP. It also serves as its identifier. | getIp(): ?string | setIp(?string ip): void |
| `locked` | `?bool` | Optional | A boolean value indicating whether or not the floating IP has pending actions preventing new ones from being submitted. | getLocked(): ?bool | setLocked(?bool locked): void |
| `projectId` | `?string` | Optional | The UUID of the project to which the reserved IP currently belongs. | getProjectId(): ?string | setProjectId(?string projectId): void |
| `region` | [`?Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region.md) | Optional | - | getRegion(): ?Region | setRegion(?Region region): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\FloatingIp1Builder;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;

$floatingIp1 = FloatingIp1Builder::init()
    ->droplet(
        ApiHelper::deserialize('{"key1":"val1","key2":"val2"}')
    )
    ->ip('45.55.96.47')
    ->locked(true)
    ->projectId('746c6152-2fa2-11ed-92d3-27aaa54e4988')
    ->region(
        RegionBuilder::init(
            false,
            [
                'features7',
                'features8',
                'features9'
            ],
            'name6',
            [
                'sizes6'
            ],
            'slug0'
        )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



