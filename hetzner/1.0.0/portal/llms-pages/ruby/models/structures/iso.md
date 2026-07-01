# Iso

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRklzbw


# Class Name

`Iso`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `String` | Required | ISO 8601 timestamp of deprecation, null if ISO is still available. After the deprecation time it will no longer be possible to attach the ISO to Servers. |
| `description` | `String` | Required | Description of the ISO |
| `id` | `Integer` | Required | ID of the Resource |
| `name` | `String` | Required | Unique identifier of the ISO. Only set for public ISOs |
| `type` | [`Type26Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-26.md) | Required | Type of the ISO |


# Example

```ruby
iso = Iso.new(
  '2018-02-28T00:00:00+00:00',
  'FreeBSD 11.0 x64',
  42,
  'FreeBSD-11.0-RELEASE-amd64-dvd1',
  Type26Enum::PUBLIC
)
```



