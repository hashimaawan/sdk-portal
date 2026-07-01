# Ssh Keys Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaCUyNTIwS2V5cyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`SshKeysResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `ssh_key` | [`SshKey`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/ssh-key.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
ssh_keys_response1 = SshKeysResponse1.new(
  ssh_key: SshKey.new(
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



