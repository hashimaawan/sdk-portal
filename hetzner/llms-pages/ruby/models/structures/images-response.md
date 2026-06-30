# Images Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkltYWdlcyUyNTIwUmVzcG9uc2U


# Class Name

`ImagesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `images` | [`Array[Image]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/image.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
images_response = ImagesResponse.new(
  [
    Image.new(
      nil,
      '2016-01-30T23:55:00+00:00',
      CreatedFrom.new(
        1,
        'Server'
      ),
      nil,
      '2018-02-28T00:00:00+00:00',
      'Ubuntu 20.04 Standard 64 bit',
      10,
      42,
      2.3,
      {
        'key0': 'labels0',
        'key1': 'labels1'
      },
      'ubuntu-20.04',
      OsFlavorEnum::UBUNTU,
      '20.04',
      Protection.new(
        false
      ),
      Status24Enum::AVAILABLE,
      Type22Enum::SNAPSHOT,
      false
    )
  ],
  Meta.new(
    Pagination.new(
      77.7,
      209.18,
      17.58,
      13.34,
      50.02,
      206.64
    )
  )
)
```



