# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux


# Class Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ssh_key` | [`SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/ssh-key.md) | Required | - |


# Example

```ruby
ssh_keys_response1 = SshKeysResponse1.new(
  SshKey.new(
    '2016-01-30T23:55:00+00:00',
    'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
    42,
    {
      'key0': 'labels0'
    },
    'my-resource',
    'ssh-rsa AAAjjk76kgf...Xt'
  )
)
```



