# Create Certificate Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVxdWVzdA


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
| `type` | [`Type1Enum`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/enumerations/type-1.md) | Optional | Choose between uploading a Certificate in PEM format or requesting a managed *Let's Encrypt* Certificate. If omitted defaults to `uploaded`. |


# Example

```ruby
create_certificate_request = CreateCertificateRequest.new(
  'my website cert',
  '-----BEGIN CERTIFICATE-----\n...',
  [
    'domain_names2'
  ],
  { 'key1' => 'val1', 'key2' => 'val2' },
  '-----BEGIN PRIVATE KEY-----\n...',
  Type1Enum::UPLOADED
)
```



