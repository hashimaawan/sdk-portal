# Ssh Keys Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVxdWVzdA


# Class Name

`SshKeysRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the SSH key |
| `public_key` | `String` | Required | Public key |


# Example

```ruby
ssh_keys_request = SshKeysRequest.new(
  'My ssh key',
  'ssh-rsa AAAjjk76kgf...Xt',
  { 'key1' => 'val1', 'key2' => 'val2' }
)
```



