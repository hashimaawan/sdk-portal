# V2 Apps Regions Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBBcHBzJTI1MjBSZWdpb25zJTI1MjBSZXNwb25zZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2AppsRegionsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `regions` | [`?(GeographicalInformationAboutAnAppOrigin[])`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/geographical-information-about-an-app-origin.md) | Optional | - | getRegions(): ?array | setRegions(?array regions): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2AppsRegionsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\GeographicalInformationAboutAnAppOriginBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2AppsRegionsResponse = V2AppsRegionsResponseBuilder::init()
    ->regions(
        [
            GeographicalInformationAboutAnAppOriginBuilder::init()
                ->continent('continent2')
                ->dataCenters(
                    [
                        'data_centers9'
                    ]
                )
                ->default(false)
                ->disabled(false)
                ->flag('flag4')
                ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                ->build()
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



