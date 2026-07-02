# V2 Volumes Snapshots Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlcXVlc3Q

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2VolumesSnapshotsRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `name` | `string` | Required | A human-readable name for the volume snapshot. | getName(): string | setName(string name): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2VolumesSnapshotsRequestBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2VolumesSnapshotsRequest = V2VolumesSnapshotsRequestBuilder::init(
    'big-data-snapshot1475261774'
)
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



