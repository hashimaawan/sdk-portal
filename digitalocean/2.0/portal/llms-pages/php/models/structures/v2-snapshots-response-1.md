# V2 Snapshots Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBTbmFwc2hvdHMlMjUyMFJlc3BvbnNlMQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2SnapshotsResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `snapshot` | [`?Snapshot`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/snapshot.md) | Optional | - | getSnapshot(): ?Snapshot | setSnapshot(?Snapshot snapshot): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2SnapshotsResponse1Builder;
use DigitalOceanApiLib\Models\Builders\SnapshotBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\ResourceType1;
use DigitalOceanApiLib\ApiHelper;

$v2SnapshotsResponse1 = V2SnapshotsResponse1Builder::init()
    ->snapshot(
        SnapshotBuilder::init(
            'id8',
            DateTimeHelper::fromRfc3339DateTimeRequired('2016-03-13T12:52:32.123Z'),
            36,
            'name8',
            [
                'regions3',
                'regions4',
                'regions5'
            ],
            140.04,
            'resource_id4',
            ResourceType1::DROPLET
        )
            ->tags(
                [
                    'tags3'
                ]
            )
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



