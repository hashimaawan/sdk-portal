# Floating Ip 1 Droplet

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/python/x-redirect/JTI0bSUyRkZsb2F0aW5nSXAxRHJvcGxldA


# Data Type

`Any | None | Droplet`


# Cases

| Type |
|  --- |
| [`Any`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/object.md) |
| [`Droplet`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/python/models/structures/droplet.md) |


# Any

## Initialization Code

### Example

```python
value = jsonpickle.decode('{"key1":"val1","key2":"val2"}')
```


# Droplet

## Initialization Code

### Example

```python
value = Droplet(
    backup_ids=[
        53893572
    ],
    created_at=dateutil.parser.parse('2020-07-21T18:37:44Z'),
    disk=25,
    features=[
        'backups',
        'private_networking',
        'ipv6'
    ],
    id=3164444,
    image=Image1(
        created_at=dateutil.parser.parse('2020-05-04T22:23:02Z'),
        distribution=Distribution.UBUNTU,
        id=7555620,
        min_disk_size=20,
        name='Nifty New Snapshot',
        public=True,
        regions=[
            Region2.NYC1,
            Region2.NYC2
        ],
        size_gigabytes=2.34,
        slug='nifty1',
        status=Status7.NEW,
        tags=[
            'base-image',
            'prod'
        ],
        mtype=Type9.SNAPSHOT
    ),
    locked=False,
    memory=1024,
    name='example.com',
    networks=Networks(),
    next_backup_window=NextBackupWindow(
        end=dateutil.parser.parse('2019-12-04T23:00:00Z'),
        start=dateutil.parser.parse('2019-12-04T00:00:00Z')
    ),
    region=Region(
        available=True,
        features=[
            'private_networking',
            'backups',
            'ipv6',
            'metadata',
            'install_agent',
            'storage',
            'image_transfer'
        ],
        name='New York 3',
        sizes=[
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
        slug='nyc3'
    ),
    size=Size(
        available=True,
        description='Basic',
        disk=25,
        memory=1024,
        price_hourly=0.00743999984115362,
        price_monthly=5,
        regions=[
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
        slug='s-1vcpu-1gb',
        transfer=1,
        vcpus=1
    ),
    size_slug='s-1vcpu-1gb',
    snapshot_ids=[
        67512819
    ],
    status=Status8.ACTIVE,
    tags=[
        'web',
        'env:prod'
    ],
    vcpus=1,
    volume_ids=[
        '506f78a4-e098-11e5-ad9f-000f53306ae1'
    ],
    vpc_uuid='760e09ef-dc84-11e8-981e-3cfdfeaae000'
)
```



