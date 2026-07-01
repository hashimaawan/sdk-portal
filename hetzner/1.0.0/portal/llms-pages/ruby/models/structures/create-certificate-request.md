# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA

*This model accepts additional fields of type Object.*


# Class Name

`CreateCertificateRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | `String` | Optional | Certificate and chain in PEM format, in order so that each record directly certifies the one preceding. Required for type `uploaded` Certificates. |
| `domain_names` | `Array[String]` | Optional | Domains and subdomains that should be contained in the Certificate issued by *Let's Encrypt*. Required for type `managed` Certificates. |
| `labels` | `Object` | Optional | User-defined labels (key-value pairs) |
| `name` | `String` | Required | Name of the Certificate |
| `private_key` | `String` | Optional | Certificate key in PEM format. Required for type `uploaded` Certificates. |
| `type` | [`Type1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
create_certificate_request = CreateCertificateRequest.new(
  name: 'my website cert',
  certificate: '-----BEGIN CERTIFICATE-----\n...',
  domain_names: [
    'domain_names2'
  ],
  labels: { 'key1' => 'val1', 'key2' => 'val2' },
  private_key: '-----BEGIN PRIVATE KEY-----\n...',
  type: Type1::UPLOADED,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



