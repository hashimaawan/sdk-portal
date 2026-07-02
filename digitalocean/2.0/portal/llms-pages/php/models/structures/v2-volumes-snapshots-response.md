# V2 Volumes Snapshots Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNl

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2VolumesSnapshotsResponse`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `snapshot` | [`?Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/snapshot.md) | Optional | - | getSnapshot(): ?Snapshot | setSnapshot(?Snapshot snapshot): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2VolumesSnapshotsResponseBuilder;
use DigitalOceanApiLib\Models\Builders\SnapshotBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\ResourceType1;
use DigitalOceanApiLib\ApiHelper;

$v2VolumesSnapshotsResponse = V2VolumesSnapshotsResponseBuilder::init()
    ->snapshot(
        SnapshotBuilder::init(
            '8fa70202-873f-11e6-8b68-000f533176b1',
            DateTimeHelper::fromRfc3339DateTimeRequired('2020-09-30T18:56:14Z'),
            10,
            'big-data-snapshot1475261774',
            [
                'nyc1'
            ],
            10,
            '82a48a18-873f-11e6-96bf-000f53315a41',
            ResourceType1::VOLUME
        )
            ->tags(
                [
                    'aninterestingtag'
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



