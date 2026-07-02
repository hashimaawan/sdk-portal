# V2 Reports Droplet Neighbors Ids Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBSZXBvcnRzJTI1MjBEcm9wbGV0JTI1MjBOZWlnaGJvcnMlMjUyMElkcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2ReportsDropletNeighborsIdsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `neighborIds` | `?(int[][])` | Optional | An array of arrays. Each array will contain a set of Droplet IDs for Droplets that share a physical server. | getNeighborIds(): ?array | setNeighborIds(?array neighborIds): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2ReportsDropletNeighborsIdsResponseBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2ReportsDropletNeighborsIdsResponse = V2ReportsDropletNeighborsIdsResponseBuilder::init()
    ->neighborIds(
        [
            [
                168671828,
                168663509,
                168671815
            ],
            [
                168671883,
                168671750
            ]
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



