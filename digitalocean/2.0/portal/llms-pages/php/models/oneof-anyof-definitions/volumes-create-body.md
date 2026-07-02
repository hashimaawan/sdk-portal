# Volumes Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRlZvbHVtZXNDcmVhdGVCb2R5


# Data Type

`V2VolumesRequest|V2VolumesRequest1`


# Cases

| Type |
|  --- |
| [`V2VolumesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-volumes-request.md) |
| [`V2VolumesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/v2-volumes-request-1.md) |


# V2VolumesRequest

## Initialization Code

### Example

```php
$value = V2VolumesRequestBuilder::init(
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
    ->build();
```


# V2VolumesRequest1

## Initialization Code

### Example

```php
$value = V2VolumesRequest1Builder::init(
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
    ->build();
```



