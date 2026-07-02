# Volume

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Volume`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `createdAt` | `?string` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the block storage volume was created. | getCreatedAt(): ?string | setCreatedAt(?string createdAt): void |
| `description` | `?string` | Optional | An optional free-form text field to describe a block storage volume. | getDescription(): ?string | setDescription(?string description): void |
| `dropletIds` | `?(int[])` | Optional, Read-only | An array containing the IDs of the Droplets the volume is attached to. Note that at this time, a volume can only be attached to a single Droplet. | getDropletIds(): ?array | setDropletIds(?array dropletIds): void |
| `id` | `?string` | Optional, Read-only | The unique identifier for the block storage volume. | getId(): ?string | setId(?string id): void |
| `name` | `?string` | Optional | A human-readable name for the block storage volume. Must be lowercase and be composed only of numbers, letters and "-", up to a limit of 64 characters. The name must begin with a letter. | getName(): ?string | setName(?string name): void |
| `sizeGigabytes` | `?int` | Optional | The size of the block storage volume in GiB (1024^3). | getSizeGigabytes(): ?int | setSizeGigabytes(?int sizeGigabytes): void |
| `tags` | `?(string[])` | Optional | A flat array of tag names as strings to be applied to the resource. Tag names may be for either existing or new tags. | getTags(): ?array | setTags(?array tags): void |
| `filesystemLabel` | `?string` | Optional | The label currently applied to the filesystem. | getFilesystemLabel(): ?string | setFilesystemLabel(?string filesystemLabel): void |
| `filesystemType` | `?string` | Optional | The type of filesystem currently in-use on the volume. | getFilesystemType(): ?string | setFilesystemType(?string filesystemType): void |
| `region` | [`?Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region.md) | Optional, Read-only | - | getRegion(): ?Region | setRegion(?Region region): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\VolumeBuilder;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;

$volume = VolumeBuilder::init()
    ->createdAt('2020-03-02T17:00:49Z')
    ->description('Block store for examples')
    ->dropletIds(
        []
    )
    ->id('506f78a4-e098-11e5-ad9f-000f53306ae1')
    ->name('example')
    ->sizeGigabytes(10)
    ->tags(
        [
            'base-image',
            'prod'
        ]
    )
    ->filesystemLabel('example')
    ->filesystemType('ext4')
    ->region(
        RegionBuilder::init(
            true,
            [
                'private_networking',
                'backups',
                'ipv6',
                'metadata'
            ],
            'New York 1',
            [
                's-1vcpu-1gb',
                's-1vcpu-2gb',
                's-1vcpu-3gb',
                's-2vcpu-2gb',
                's-3vcpu-1gb',
                's-2vcpu-4gb',
                's-4vcpu-8gb',
                's-6vcpu-16gb',
                's-8vcpu-32gb',
                's-12vcpu-48gb',
                's-16vcpu-64gb',
                's-20vcpu-96gb',
                's-24vcpu-128gb',
                's-32vcpu-192gb'
            ],
            'nyc1'
        )->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



