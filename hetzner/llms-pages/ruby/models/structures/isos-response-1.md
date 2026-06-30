# Isos Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRklzb3MlMjUyMFJlc3BvbnNlMQ


# Class Name

`IsosResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `iso` | [`Iso`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/iso.md) | Required | - |


# Example

```ruby
isos_response1 = IsosResponse1.new(
  Iso.new(
    '2018-02-28T00:00:00+00:00',
    'FreeBSD 11.0 x64',
    42,
    'FreeBSD-11.0-RELEASE-amd64-dvd1',
    Type26Enum::PUBLIC
  )
)
```



