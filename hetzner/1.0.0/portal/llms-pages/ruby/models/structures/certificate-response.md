# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/certificate.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
certificate_response = CertificateResponse.new(
  certificate: Certificate.new(
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



