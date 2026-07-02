# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `created_at` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents when the certificate was created. |
| `dns_names` | `Array[String]` | Optional | An array of fully qualified domain names (FQDNs) for which the certificate was issued. |
| `id` | `UUID \| String` | Optional, Read-only | A unique ID that can be used to identify and reference a certificate. |
| `name` | `String` | Optional | A unique human-readable name referring to a certificate. |
| `not_after` | `DateTime` | Optional, Read-only | A time value given in ISO8601 combined date and time format that represents the certificate's expiration date. |
| `sha_1_fingerprint` | `String` | Optional, Read-only | A unique identifier generated from the SHA-1 fingerprint of the certificate. |
| `state` | [`State`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/state.md) | Optional, Read-only | A string representing the current state of the certificate. It may be `pending`, `verified`, or `error`. |
| `type` | [`Type4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/enumerations/type-4.md) | Optional | A string representing the type of the certificate. The value will be `custom` for a user-uploaded certificate or `lets_encrypt` for one automatically generated with Let's Encrypt. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
certificate = Certificate.new(
  created_at: DateTimeHelper.from_rfc3339('2017-02-08T16:02:37Z'),
  dns_names: [
    'www.example.com',
    'example.com'
  ],
  id: '892071a0-bb95-49bc-8021-3afd67a210bf',
  name: 'web-cert-01',
  not_after: DateTimeHelper.from_rfc3339('2017-02-22T00:23:00Z'),
  sha1_fingerprint: 'dfcc9f57d86bf58e321c2c6c31c7a971be244ac7',
  state: State::VERIFIED,
  type: Type4::LETS_ENCRYPT,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



