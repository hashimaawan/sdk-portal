# Images Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`ImagesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `image` | [`Image`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/image.md) | Optional | - |


# Example

```ruby
images_response1 = ImagesResponse1.new(
  Image.new(
    186,
    'created6',
    CreatedFrom.new(
      60,
      'name6'
    ),
    'deleted4',
    'deprecated8',
    'description6',
    244.18,
    128,
    141.34,
    {
      'key0': 'labels4'
    },
    'name6',
    OsFlavorEnum::DEBIAN,
    'os_version4',
    Protection.new(
      false
    ),
    Status24Enum::UNAVAILABLE,
    Type22Enum::APP,
    false
  )
)
```



