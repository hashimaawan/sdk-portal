# Ssh Keys Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2U


# Class Name

`SshKeysResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/meta.md) | Optional | - |
| `ssh_keys` | [`Array[SshKey]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ssh-key.md) | Required | - |


# Example

```ruby
ssh_keys_response = SshKeysResponse.new(
  [
    SshKey.new(
      '2016-01-30T23:55:00+00:00',
      'b7:2f:30:a0:2f:6c:58:6c:21:04:58:61:ba:06:3b:2f',
      42,
      {
        'key0': 'labels4',
        'key1': 'labels5',
        'key2': 'labels6'
      },
      'my-resource',
      'ssh-rsa AAAjjk76kgf...Xt'
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



