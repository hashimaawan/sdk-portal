# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type Object.*


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
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ssh_key = SshKey.new(
  created: '2016-01-30T23:55:00+00:00',
  fingerprint: 'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
  id: 42,
  labels: {
    'key0' => 'labels0'
  },
  name: 'my-resource',
  public_key: 'ssh-rsa AAAjjk76kgf...Xt',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



