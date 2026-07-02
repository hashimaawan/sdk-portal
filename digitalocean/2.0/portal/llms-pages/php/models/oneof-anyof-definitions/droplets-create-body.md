# Droplets Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/php/x-redirect/JTI0bSUyRkRyb3BsZXRzQ3JlYXRlQm9keQ


# Data Type

`SingleDropletRequest|MultipleDropletRequest`


# Cases

| Type |
|  --- |
| [`SingleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/single-droplet-request.md) |
| [`MultipleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/php/models/structures/multiple-droplet-request.md) |


# SingleDropletRequest

## Initialization Code

### Example

```php
$value = SingleDropletRequestBuilder::init(
    'example.com',
    'ubuntu-20-04-x64',
    's-1vcpu-1gb'
)
    ->backups(true)
    ->ipv6(true)
    ->monitoring(true)
    ->privateNetworking(true)
    ->region('nyc3')
    ->sshKeys(
        [
            289794,
            '3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45'
        ]
    )
    ->tags(
        [
            'env:prod',
            'web'
        ]
    )
    ->userData('#cloud-config
runcmd:
  - touch /test.txt
')
    ->volumes(
        [
            '12e97116-7280-11ed-b3d0-0a58ac146812'
        ]
    )
    ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
    ->withDropletAgent(true)
    ->build();
```


# MultipleDropletRequest

## Initialization Code

### Example

```php
$value = MultipleDropletRequestBuilder::init(
    [
        'sub-01.example.com',
        'sub-02.example.com'
    ],
    'ubuntu-20-04-x64',
    's-1vcpu-1gb'
)
    ->backups(true)
    ->ipv6(true)
    ->monitoring(true)
    ->privateNetworking(true)
    ->region('nyc3')
    ->sshKeys(
        [
            289794,
            '3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45'
        ]
    )
    ->tags(
        [
            'env:prod',
            'web'
        ]
    )
    ->userData('#cloud-config
runcmd:
  - touch /test.txt
')
    ->volumes(
        [
            '12e97116-7280-11ed-b3d0-0a58ac146812'
        ]
    )
    ->vpcUuid('760e09ef-dc84-11e8-981e-3cfdfeaae000')
    ->withDropletAgent(true)
    ->build();
```



