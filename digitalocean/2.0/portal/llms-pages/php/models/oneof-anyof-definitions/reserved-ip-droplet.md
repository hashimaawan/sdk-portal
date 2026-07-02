# Reserved Ip Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlJlc2VydmVkSXBEcm9wbGV0


# Data Type

`array|null|Droplet`


# Cases

| Type |
|  --- |
| [`?array`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/object.md) |
| [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/droplet.md) |


# ?array

## Initialization Code

### Example

```php
$value = ApiHelper::deserialize('{"key1":"val1","key2":"val2"}');
```


# Droplet

## Initialization Code

### Example

```php
$value = DropletBuilder::init(
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
        ->distribution(Distribution::UBUNTU)
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
        ->build(),
    false,
    1024,
    'example.com',
    NetworksBuilder::init()->build(),
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
    )->build(),
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
    )->build(),
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
    ->nextBackupWindow(
        NextBackupWindowBuilder::init()
            ->end(DateTimeHelper::fromRfc3339DateTime('2019-12-04T23:00:00Z'))
            ->start(DateTimeHelper::fromRfc3339DateTime('2019-12-04T00:00:00Z'))
            ->build()
    )
    ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
    ->build();
```



