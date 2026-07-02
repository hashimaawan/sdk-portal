# Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRyb3BsZXQ

*This model accepts additional fields of type [array](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md).*


# Class Name

`Droplet`


# Fields

| Name | Type | Tags | Description | Getter | Setter |
|  --- | --- | --- | --- | --- | --- |
| `backupIds` | `int[]` | Required | An array of backup IDs of any backups that have been taken of the Droplet instance.  Droplet backups are enabled at the time of the instance creation. | getBackupIds(): array | setBackupIds(array backupIds): void |
| `createdAt` | `DateTime` | Required | A time value given in ISO8601 combined date and time format that represents when the Droplet was created. | getCreatedAt(): \DateTime | setCreatedAt(\DateTime createdAt): void |
| `disk` | `int` | Required | The size of the Droplet's disk in gigabytes. | getDisk(): int | setDisk(int disk): void |
| `features` | `string[]` | Required | An array of features enabled on this Droplet. | getFeatures(): array | setFeatures(array features): void |
| `id` | `int` | Required | A unique identifier for each Droplet instance. This is automatically generated upon Droplet creation. | getId(): int | setId(int id): void |
| `image` | [`Image1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/image-1.md) | Required | - | getImage(): Image1 | setImage(Image1 image): void |
| `kernel` | [`?Kernel`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/kernel.md) | Optional | **Note**: All Droplets created after March 2017 use internal kernels by default.<br>These Droplets will have this attribute set to `null`.<br><br>The current [kernel](https://www.digitalocean.com/docs/droplets/how-to/kernel/)<br>for Droplets with externally managed kernels. This will initially be set to<br>the kernel of the base image when the Droplet is created. | getKernel(): ?Kernel | setKernel(?Kernel kernel): void |
| `locked` | `bool` | Required | A boolean value indicating whether the Droplet has been locked, preventing actions by users. | getLocked(): bool | setLocked(bool locked): void |
| `memory` | `int` | Required | Memory of the Droplet in megabytes.<br><br>**Constraints**: *Multiple Of*: `8` | getMemory(): int | setMemory(int memory): void |
| `name` | `string` | Required | The human-readable name set for the Droplet instance. | getName(): string | setName(string name): void |
| `networks` | [`Networks`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/networks.md) | Required | The details of the network that are configured for the Droplet instance.  This is an object that contains keys for IPv4 and IPv6.  The value of each of these is an array that contains objects describing an individual IP resource allocated to the Droplet.  These will define attributes like the IP address, netmask, and gateway of the specific network depending on the type of network it is. | getNetworks(): Networks | setNetworks(Networks networks): void |
| `nextBackupWindow` | [`?NextBackupWindow`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/next-backup-window.md) | Required | The details of the Droplet's backups feature, if backups are configured for the Droplet. This object contains keys for the start and end times of the window during which the backup will start. | getNextBackupWindow(): ?NextBackupWindow | setNextBackupWindow(?NextBackupWindow nextBackupWindow): void |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/region.md) | Required | - | getRegion(): Region | setRegion(Region region): void |
| `size` | [`Size`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/size.md) | Required | - | getSize(): Size | setSize(Size size): void |
| `sizeSlug` | `string` | Required | The unique slug identifier for the size of this Droplet. | getSizeSlug(): string | setSizeSlug(string sizeSlug): void |
| `snapshotIds` | `int[]` | Required | An array of snapshot IDs of any snapshots created from the Droplet instance. | getSnapshotIds(): array | setSnapshotIds(array snapshotIds): void |
| `status` | [`string(Status8)`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/enumerations/status-8.md) | Required | A status string indicating the state of the Droplet instance. This may be "new", "active", "off", or "archive". | getStatus(): string | setStatus(string status): void |
| `tags` | `string[]` | Required | An array of Tags the Droplet has been tagged with. | getTags(): array | setTags(array tags): void |
| `vcpus` | `int` | Required | The number of virtual CPUs. | getVcpus(): int | setVcpus(int vcpus): void |
| `volumeIds` | `string[]` | Required | A flat array including the unique identifier for each Block Storage volume attached to the Droplet. | getVolumeIds(): array | setVolumeIds(array volumeIds): void |
| `vpcUuid` | `?string` | Optional | A string specifying the UUID of the VPC to which the Droplet is assigned. | getVpcUuid(): ?string | setVpcUuid(?string vpcUuid): void |
| `additionalProperties` | [`array<string, array>`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) | Optional | - | findAdditionalProperty(string key): array | additionalProperty(string key, array value): void |


# Example

```php
use DigitalOceanApiLib\Models\Builders\DropletBuilder;
use DigitalOceanApiLib\Utils\DateTimeHelper;
use DigitalOceanApiLib\Models\Builders\Image1Builder;
use DigitalOceanApiLib\Models\Distribution;
use DigitalOceanApiLib\Models\Region2;
use DigitalOceanApiLib\Models\Status7;
use DigitalOceanApiLib\Models\Type9;
use DigitalOceanApiLib\ApiHelper;
use DigitalOceanApiLib\Models\Builders\NetworksBuilder;
use DigitalOceanApiLib\Models\Builders\V4Builder;
use DigitalOceanApiLib\Models\Type10;
use DigitalOceanApiLib\Models\Builders\V6Builder;
use DigitalOceanApiLib\Models\Type11;
use DigitalOceanApiLib\Models\Builders\RegionBuilder;
use DigitalOceanApiLib\Models\Builders\SizeBuilder;
use DigitalOceanApiLib\Models\Status8;
use DigitalOceanApiLib\Models\Builders\KernelBuilder;
use DigitalOceanApiLib\Models\Builders\NextBackupWindowBuilder;

$droplet = DropletBuilder::init(
    [
        53893572
    ],
    DateTimeHelper::fromRfc3339DateTimeRequired('2020-07-21T18:37:44Z'),
    25,
    [
        'backups',
        'private_networking',
        'ipv6'
    ],
    3164444,
    Image1Builder::init()
        ->createdAt(DateTimeHelper::fromRfc3339DateTime('2020-05-04T22:23:02Z'))
        ->description('description6')
        ->distribution(Distribution::UBUNTU)
        ->errorMessage('error_message8')
        ->id(7555620)
        ->minDiskSize(20)
        ->name('Nifty New Snapshot')
        ->public(true)
        ->regions(
            [
                Region2::NYC1,
                Region2::NYC2
            ]
        )
        ->sizeGigabytes(2.34)
        ->slug('nifty1')
        ->status(Status7::NEW_)
        ->tags(
            [
                'base-image',
                'prod'
            ]
        )
        ->type(Type9::SNAPSHOT)
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    false,
    1024,
    'example.com',
    NetworksBuilder::init()
        ->v4(
            [
                V4Builder::init()
                    ->gateway('gateway2')
                    ->ipAddress('ip_address2')
                    ->netmask('netmask2')
                    ->type(Type10::PUBLIC_)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                V4Builder::init()
                    ->gateway('gateway2')
                    ->ipAddress('ip_address2')
                    ->netmask('netmask2')
                    ->type(Type10::PUBLIC_)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                V4Builder::init()
                    ->gateway('gateway2')
                    ->ipAddress('ip_address2')
                    ->netmask('netmask2')
                    ->type(Type10::PUBLIC_)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->v6(
            [
                V6Builder::init()
                    ->gateway('gateway4')
                    ->ipAddress('ip_address4')
                    ->netmask(106)
                    ->type(Type11::PUBLIC_)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build(),
                V6Builder::init()
                    ->gateway('gateway4')
                    ->ipAddress('ip_address4')
                    ->netmask(106)
                    ->type(Type11::PUBLIC_)
                    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
                    ->build()
            ]
        )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    RegionBuilder::init(
        true,
        [
            'private_networking',
            'backups',
            'ipv6',
            'metadata',
            'install_agent',
            'storage',
            'image_transfer'
        ],
        'New York 3',
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
            's-32vcpu-192g'
        ],
        'nyc3'
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    SizeBuilder::init(
        true,
        'Basic',
        25,
        1024,
        0.00743999984115362,
        5,
        [
            'ams2',
            'ams3',
            'blr1',
            'fra1',
            'lon1',
            'nyc1',
            'nyc2',
            'nyc3',
            'sfo1',
            'sfo2',
            'sfo3',
            'sgp1',
            'tor1'
        ],
        's-1vcpu-1gb',
        1,
        1
    )
        ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
        ->build(),
    's-1vcpu-1gb',
    [
        67512819
    ],
    Status8::ACTIVE,
    [
        'web',
        'env:prod'
    ],
    1,
    [
        '506f78a4-e098-11e5-ad9f-000f53306ae1'
    ]
)
    ->kernel(
        KernelBuilder::init()
            ->id(16)
            ->name('name4')
            ->version('version0')
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->nextBackupWindow(
        NextBackupWindowBuilder::init()
            ->end(DateTimeHelper::fromRfc3339DateTime('2019-12-04T23:00:00Z'))
            ->start(DateTimeHelper::fromRfc3339DateTime('2019-12-04T00:00:00Z'))
            ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
            ->build()
    )
    ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
    ->additionalProperty('exampleAdditionalProperty', ApiHelper::deserialize('{"key1":"val1","key2":"val2"}'))
    ->build();
```



