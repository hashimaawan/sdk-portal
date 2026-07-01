# Certificate

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNlcnRpZmljYXRl

*This model accepts additional fields of type Object.*


# Class Name

`Certificate`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | `String` | Required | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding |
| `created` | `String` | Required | Point in time when the Resource was created (in ISO-8601 format) |
| `domain_names` | `Array[String]` | Required | Domains and subdomains covered by the Certificate |
| `fingerprint` | `String` | Required | SHA256 fingerprint of the Certificate |
| `id` | `Integer` | Required | ID of the Resource |
| `labels` | `Hash[String, String]` | Required | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Resource. Must be unique per Project. |
| `not_valid_after` | `String` | Required | Point in time when the Certificate stops being valid (in ISO-8601 format) |
| `not_valid_before` | `String` | Required | Point in time when the Certificate becomes valid (in ISO-8601 format) |
| `status` | [`Status2`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/status-2.md) | Optional | Current status of a type `managed` Certificate, always *null* for type `uploaded` Certificates |
| `type` | [`Type`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type.md) | Optional | Type of the Certificate |
| `used_by` | [`Array[UsedBy]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/used-by.md) | Required | Resources currently using the Certificate |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
certificate = Certificate.new(
  certificate: '-----BEGIN CERTIFICATE-----\n...',
  created: '2016-01-30T23:55:00+00:00',
  domain_names: [
    'example.com',
    'webmail.example.com',
    'www.example.com'
  ],
  fingerprint: '03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f',
  id: 42,
  labels: {
    'key0' => 'labels8',
    'key1' => 'labels7',
    'key2' => 'labels6'
  },
  name: 'my-resource',
  not_valid_after: '2019-07-08T09:59:59+00:00',
  not_valid_before: '2019-01-08T10:00:00+00:00',
  used_by: [
    UsedBy.new(
      id: 4711,
      type: 'load_balancer',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  status: Status2.new(
    error: nil,
    issuance: Issuance::COMPLETED,
    renewal: Renewal::FAILED,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  type: Type::UPLOADED,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



