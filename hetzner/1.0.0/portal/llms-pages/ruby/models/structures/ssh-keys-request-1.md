# Ssh Keys Request 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdDE

*This model accepts additional fields of type Object.*


# Class Name

`SshKeysRequest1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Optional | New name Name to set |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ssh_keys_request1 = SshKeysRequest1.new(
  labels: { 'labelkey' => 'value' },
  name: 'My ssh key',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



