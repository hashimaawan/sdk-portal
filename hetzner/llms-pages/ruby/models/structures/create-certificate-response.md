# Create Certificate Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRkNyZWF0ZUNlcnRpZmljYXRlUmVzcG9uc2U


# Class Name

`CreateCertificateResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`NullableAction`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/nullable-action.md) | Optional | - |
| `certificate` | [`Certificate`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/certificate.md) | Required | - |


# Example

```ruby
create_certificate_response = CreateCertificateResponse.new(
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
  ),
  NullableAction.new(
    'command6',
    Error.new(
      'code2',
      'message4'
    ),
    'finished0',
    238,
    143.26,
    [
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      ),
      Resource.new(
        198,
        'type0'
      )
    ],
    'started8',
    StatusEnum::RUNNING
  )
)
```



