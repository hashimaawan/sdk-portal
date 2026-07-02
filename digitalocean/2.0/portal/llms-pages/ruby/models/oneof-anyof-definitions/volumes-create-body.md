# Volumes Create Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZXNDcmVhdGVCb2R5


# Data Type

`V2VolumesRequest | V2VolumesRequest1`


# Cases

| Type |
|  --- |
| [`V2VolumesRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-volumes-request.md) |
| [`V2VolumesRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-volumes-request-1.md) |


# V2VolumesRequest

## Initialization Code

### Example

```ruby
value = V2VolumesRequest.new(
  name: 'example',
  size_gigabytes: 10,
  region: Region2::NYC3,
  created_at: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  droplet_ids: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  tags: [
    'base-image',
    'prod'
  ],
  snapshot_id: 'b0798135-fb76-11eb-946a-0a58ac146f33',
  filesystem_type: 'ext4'
)
```


# V2VolumesRequest1

## Initialization Code

### Example

```ruby
value = V2VolumesRequest1.new(
  name: 'example',
  size_gigabytes: 10,
  region: Region2::NYC3,
  created_at: '2020-03-02T17:00:49Z',
  description: 'Block store for examples',
  droplet_ids: [],
  id: '506f78a4-e098-11e5-ad9f-000f53306ae1',
  tags: [
    'base-image',
    'prod'
  ],
  snapshot_id: 'b0798135-fb76-11eb-946a-0a58ac146f33',
  filesystem_type: 'ext4'
)
```



