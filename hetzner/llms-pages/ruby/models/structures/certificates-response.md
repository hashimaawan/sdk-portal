# Certificates Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNlcnRpZmljYXRlc1Jlc3BvbnNl


# Class Name

`CertificatesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `certificates` | [`Array[Certificate]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/certificate.md) | Required | - |
| `meta` | [`Meta`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/meta.md) | Optional | - |


# Example

```ruby
certificates_response = CertificatesResponse.new(
  [
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
        'key0': 'labels2',
        'key1': 'labels1',
        'key2': 'labels0'
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



