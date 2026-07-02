# Ssh Key

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlNzaEtleQ

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`SshKey`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `fingerprint` | `String` | Optional, Read-only | A unique identifier that differentiates this key from other keys using  a format that SSH recognizes. The fingerprint is created when the key is added to your account. |
| `id` | `Integer` | Optional, Read-only | A unique identification number for this key. Can be used to embed a  specific SSH key into a Droplet. |
| `name` | `String` | Required | A human-readable display name for this key, used to easily identify the SSH keys when they are displayed. |
| `public_key` | `String` | Required | The entire public key string that was uploaded. Embedded into the root user's `authorized_keys` file if you include this key during Droplet creation. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
ssh_key = SshKey.new(
  name: 'My SSH Public Key',
  public_key: 'ssh-rsa AEXAMPLEaC1yc2EAAAADAQABAAAAQQDDHr/jh2Jy4yALcK4JyWbVkPRaWmhck3IgCoeOO3z1e2dBowLh64QAM+Qb72pxekALga2oi4GvT+TlWNhzPH4V example',
  fingerprint: '3b:16:bf:e4:8b:00:8b:b8:59:8c:a9:d3:f0:19:45:fa',
  id: 512189,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



