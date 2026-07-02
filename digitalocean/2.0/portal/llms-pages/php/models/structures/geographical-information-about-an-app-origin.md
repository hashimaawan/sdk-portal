# Geographical Information about an App Origin

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkdlb2dyYXBoaWNhbCUyNTIwaW5mb3JtYXRpb24lMjUyMGFib3V0JTI1MjBhbiUyNTIwYXBwJTI1MjBvcmlnaW4

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`GeographicalInformationAboutAnAppOrigin`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `continent` | `?string` | Optional, Read-only | - | getContinent(): ?string | setContinent(?string continent): void |
| `dataCenters` | `?(string[])` | Optional, Read-only | - | getDataCenters(): ?array | setDataCenters(?array dataCenters): void |
| `default` | `?bool` | Optional, Read-only | Whether or not the region is presented as the default. | getDefault(): ?bool | setDefault(?bool default): void |
| `disabled` | `?bool` | Optional, Read-only | - | getDisabled(): ?bool | setDisabled(?bool disabled): void |
| `flag` | `?string` | Optional, Read-only | - | getFlag(): ?string | setFlag(?string flag): void |
| `label` | `?string` | Optional, Read-only | - | getLabel(): ?string | setLabel(?string label): void |
| `reason` | `?string` | Optional, Read-only | - | getReason(): ?string | setReason(?string reason): void |
| `slug` | `?string` | Optional, Read-only | - | getSlug(): ?string | setSlug(?string slug): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\GeographicalInformationAboutAnAppOriginBuilder;
use DigitalOceanApiLib\ApiHelper;

$geographicalInformationAboutAnAppOrigin = GeographicalInformationAboutAnAppOriginBuilder::init()
    ->continent('europe')
    ->dataCenters(
        [
            'ams'
        ]
    )
    ->default(true)
    ->disabled(true)
    ->flag('ams')
    ->label('ams')
    ->reason('to crowded')
    ->slug('basic')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



