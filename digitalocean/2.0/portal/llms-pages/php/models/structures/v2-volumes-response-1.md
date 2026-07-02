# V2 Volumes Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlYyJTI1MjBWb2x1bWVzJTI1MjBSZXNwb25zZTE

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`V2VolumesResponse1`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `volume` | [`?Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/volume.md) | Optional | - | getVolume(): ?Volume | setVolume(?Volume volume): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\V2VolumesResponse1Builder;
use DigitalOceanApiLib\Models\Builders\VolumeBuilder;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\ApiHelper;

$v2VolumesResponse1 = V2VolumesResponse1Builder::init()
    ->volume(
        VolumeBuilder::init()
            ->createdAt('2020-03-02T17:00:49Z')
            ->description('Block store for examples')
            ->dropletIds(
                []
            )
            ->id('506f78a4-e098-11e5-ad9f-000f53306ae1')
            ->name('example')
            ->sizeGigabytes(10)
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
            ->build()
    )
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



