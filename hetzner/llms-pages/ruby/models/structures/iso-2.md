# Iso 2

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRklzbzI

ISO Image that is attached to this Server. Null if no ISO is attached.


# Class Name

`Iso2`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `String` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `description` | `String` | Required | Description of the ISO |
| `id` | `Integer` | Required | ID of the Resource |
| `name` | `String` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `type` | [`Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/enumerations/type-26.md) | Required | Type of the ISO |


# Example

```ruby
iso2 = Iso2.new(
  '2018-02-28T00:00:00+00:00',
  'FreeBSD 11.0 x64',
  42,
  'FreeBSD-11.0-RELEASE-amd64-dvd1',
  Type26Enum::PUBLIC
)
```



