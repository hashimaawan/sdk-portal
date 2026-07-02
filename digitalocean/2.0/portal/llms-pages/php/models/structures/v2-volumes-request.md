# V2 Volumes Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXF1ZXN0

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2VolumesRequest`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?string` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. | getCreatedAt(): ?string | setCreatedAt(?string createdAt): void |
| `description` | `?string` | Optional | An optional free-form text field to describe a block storage volume. | getDescription(): ?string | setDescription(?string description): void |
| `dropletIds` | `?(int[])` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. | getDropletIds(): ?array | setDropletIds(?array dropletIds): void |
| `id` | `?string` | Optional, Read-only | The unique identifier for the block storage volume. | getId(): ?string | setId(?string id): void |
| `name` | `string` | Required | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. | getName(): string | setName(string name): void |
| `sizeGigabytes` | `int` | Required | The size of the block storage volume in GiB (1024^3). | getSizeGigabytes(): int | setSizeGigabytes(int sizeGigabytes): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `snapshotId` | `?string` | Optional | The unique identifier for the volume snapshot from which to create the volume. | getSnapshotId(): ?string | setSnapshotId(?string snapshotId): void |
| `filesystemType` | `?string` | Optional | The name of the filesystem type to be used on the volume. When provided, the volume will automatically be formatted to the specified filesystem type. Currently, the available options are `ext4` and `xfs`. Pre-formatted volumes are automatically mounted when attached to Ubuntu, Debian, Fedora, Fedora Atomic, and CentOS Droplets created on or after April 26, 2018. Attaching pre-formatted volumes to other Droplets is not recommended. | getFilesystemType(): ?string | setFilesystemType(?string filesystemType): void |
| `filesystemLabel` | `?string` | Optional | **Constraints**: *Maximum Length*: `16` | getFilesystemLabel(): ?string | setFilesystemLabel(?string filesystemLabel): void |
| `region` | [`string(Region2)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/region-2.md) | Required | The slug identifier for the region where the resource will initially be  available. | getRegion(): string | setRegion(string region): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2VolumesRequestBuilder;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\ApiHelper;

$v2VolumesRequest = V2VolumesRequestBuilder::init(
    'example',
    10,
    Region2::NYC3
)
    ->createdAt('2020-03-02T17:00:49Z')
    ->description('Block store for examples')
    ->dropletIds(
        []
    )
    ->id('506f78a4-e098-11e5-ad9f-000f53306ae1')
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->snapshotId('b0798135-fb76-11eb-946a-0a58ac146f33')
    ->filesystemType('ext4')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



