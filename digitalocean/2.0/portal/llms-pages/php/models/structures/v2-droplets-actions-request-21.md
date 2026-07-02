# V2 Droplets Actions Request 21

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBEcm9wbGV0cyUyNTIwQWN0aW9ucyUyNTIwUmVxdWVzdDIx

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2DropletsActionsRequest21`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `type` | [`string(Type12)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-12.md) | Required | The type of action to initiate for the Droplet. | getType(): string | setType(string type): void |
| `disk` | `?bool` | Optional | When `true`, the Droplet's disk will be resized in addition to its RAM and CPU. This is a permanent change and cannot be reversed as a Droplet's disk size cannot be decreased. | getDisk(): ?bool | setDisk(?bool disk): void |
| `size` | `?string` | Optional | The slug identifier for the size to which you wish to resize the Droplet. | getSize(): ?string | setSize(?string size): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2DropletsActionsRequest21Builder;
use DigitalOceanApiLib\Models\Type12;
use DigitalOceanApiLib\ApiHelper;

$v2DropletsActionsRequest21 = V2DropletsActionsRequest21Builder::init(
    Type12::REBOOT
)
    ->disk(true)
    ->size('s-2vcpu-2gb')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



