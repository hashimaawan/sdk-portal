# Droplets Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRyb3BsZXRzQ3JlYXRlQm9keQ


# Data Type

`SingleDropletRequest | MultipleDropletRequest`


# Cases

| Type |
|  --- |
| [`SingleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/single-droplet-request.md) |
| [`MultipleDropletRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/multiple-droplet-request.md) |


# SingleDropletRequest

## Initialization Code

### Example

```ruby
value = SingleDropletRequest.new(
  name: 'example.com',
  image: 'ubuntu-20-04-x64',
  size: 's-1vcpu-1gb',
  backups: true,
  ipv6: true,
  monitoring: true,
  private_networking: true,
  region: 'nyc3',
  ssh_keys: [
    289794,
    '3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45'
  ],
  tags: [
    'env:prod',
    'web'
  ],
  user_data: '#cloud-config\nruncmd:\n  - touch /test.txt\n',
  volumes: [
    '12e97116-7280-11ed-b3d0-0a58ac146812'
  ],
  vpc_uuid: '760e09ef-dc84-11e8-981e-3cfdfeaae000',
  with_droplet_agent: true
)
```


# MultipleDropletRequest

## Initialization Code

### Example

```ruby
value = MultipleDropletRequest.new(
  names: [
    'sub-01.example.com',
    'sub-02.example.com'
  ],
  image: 'ubuntu-20-04-x64',
  size: 's-1vcpu-1gb',
  backups: true,
  ipv6: true,
  monitoring: true,
  private_networking: true,
  region: 'nyc3',
  ssh_keys: [
    289794,
    '3b:16:e4:bf:8b:00:8b:b8:59:8c:a9:d3:f0:19:fa:45'
  ],
  tags: [
    'env:prod',
    'web'
  ],
  user_data: '#cloud-config\nruncmd:\n  - touch /test.txt\n',
  volumes: [
    '12e97116-7280-11ed-b3d0-0a58ac146812'
  ],
  vpc_uuid: '760e09ef-dc84-11e8-981e-3cfdfeaae000',
  with_droplet_agent: true
)
```



