# V2 Volumes Actions Request 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBBY3Rpb25zJTI1MjBSZXF1ZXN0Mg

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2VolumesActionsRequest2`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `region` | [`?string(Region2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-2.md) | Optional | The slug identifier for the region where the resource will initially be  available. | getRegion(): ?string | setRegion(?string region): void |
| `type` | [`string(Type21)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/type-21.md) | Required | The volume action to initiate. | getType(): string | setType(string type): void |
| `sizeGigabytes` | `int` | Required | The new size of the block storage volume in GiB (1024^3).<br><br>**Constraints**: `<= 16384` | getSizeGigabytes(): int | setSizeGigabytes(int sizeGigabytes): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2VolumesActionsRequest2Builder;
use DigitalOceanApiLib\Models\Type21;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\ApiHelper;

$v2VolumesActionsRequest2 = V2VolumesActionsRequest2Builder::init(
    Type21::ATTACH,
    15384
)
    ->region(Region2::NYC3)
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



