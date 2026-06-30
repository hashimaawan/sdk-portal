# Isos Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNl


# Class Name

`IsosResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `isos` | [`Array[Iso]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/iso.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
isos_response = IsosResponse.new(
  [
    Iso.new(
      '2018-02-28T00:00:00+00:00',
      'FreeBSD 11.0 x64',
      42,
      'FreeBSD-11.0-RELEASE-amd64-dvd1',
      Type26Enum::PUBLIC
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



