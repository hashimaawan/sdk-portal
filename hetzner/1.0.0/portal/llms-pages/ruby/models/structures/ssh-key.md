# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaEtleQ


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `fingerprint` | `String` | Required | Fingerprint of public key |
| `id` | `Integer` | Required | ID of the Resource |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `public_key` | `String` | Required | Public key |


# Example

```ruby
ssh_key = SshKey.new(
  '2016-01-30T23:55:00+00:00',
  'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
  42,
  {
    'key0': 'labels0'
  },
  'my-resource',
  'ssh-rsa AAAjjk76kgf...Xt'
)
```



