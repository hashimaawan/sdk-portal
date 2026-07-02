# V2 Droplets Actions Request 22

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDIy

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsActionsRequest22`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`string(Type12)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | getType(): string | setType(string type): void |
| `image` | string\|int\|null | Optional | This is a container for one-of cases. | getImage(): | setImage( image): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsActionsRequest22Builder;
use DigitalOceanApiLib\Models\Type12;
use DigitalOceanApiLib\ApiHelper;

$v2DropletsActionsRequest22 = V2DropletsActionsRequest22Builder::init(
    Type12::REBOOT
)
    ->image(
        'ubuntu-20-04-x64'
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



