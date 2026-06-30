# Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/certificate.md) | Required | - |


# Example

```ruby
certificate_response = CertificateResponse.new(
  Certificate.new(
    '-----BEGIN CERTIFICATE-----\n...',
    '2016-01-30T23:55:00+00:00',
    [
      'example.com',
      'webmail.example.com',
      'www.example.com'
    ],
    '03:c7:55:9b:2a:d1:04:17:09:f6:d0:7f:18:34:63:d4:3e:5f',
    42,
    {
      'key0': 'labels8',
      'key1': 'labels7',
      'key2': 'labels6'
    },
    'my-resource',
    '2019-07-08T09:59:59+00:00',
    '2019-01-08T10:00:00+00:00',
    [
      UsedBy.new(
        4711,
        'load_balancer'
      )
    ],
    Status2.new(
      nil,
      IssuanceEnum::COMPLETED,
      RenewalEnum::FAILED
    ),
    TypeEnum::UPLOADED
  )
)
```



