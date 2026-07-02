# Volume Actions Post by Id Body

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlZvbHVtZUFjdGlvbnNQb3N0QnlJZEJvZHk


# Data Type

`V2VolumesActionsRequest | V2VolumesActionsRequest1 | V2VolumesActionsRequest2`


# Cases

| Type |
|  --- |
| [`V2VolumesActionsRequest`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-volumes-actions-request.md) |
| [`V2VolumesActionsRequest1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-volumes-actions-request-1.md) |
| [`V2VolumesActionsRequest2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/v2-volumes-actions-request-2.md) |


# V2VolumesActionsRequest

## Initialization Code

### Example

```ruby
value = V2VolumesActionsRequest.new(
  type: Type21::ATTACH,
  droplet_id: 11612190,
  region: Region2::NYC3,
  tags: [
    'base-image',
    'prod'
  ]
)
```


# V2VolumesActionsRequest1

## Initialization Code

### Example

```ruby
value = V2VolumesActionsRequest1.new(
  type: Type21::ATTACH,
  droplet_id: 11612190,
  region: Region2::NYC3
)
```


# V2VolumesActionsRequest2

## Initialization Code

### Example

```ruby
value = V2VolumesActionsRequest2.new(
  type: Type21::ATTACH,
  size_gigabytes: 15384,
  region: Region2::NYC3
)
```



