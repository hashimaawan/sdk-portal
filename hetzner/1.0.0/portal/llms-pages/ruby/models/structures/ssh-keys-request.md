# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the SSH key |
| `public_key` | `String` | Required | Public key |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ssh_keys_request = SshKeysRequest.new(
  name: 'My ssh key',
  public_key: 'ssh-rsa AAAjjk76kgf...Xt',
  labels: { 'key1' => 'val1', 'key2' => 'val2' },
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



