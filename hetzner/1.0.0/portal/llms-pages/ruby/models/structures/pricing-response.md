# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/pricing.md) | Required | - |


# Example

```ruby
pricing_response = PricingResponse.new(
  Pricing.new(
    'EUR',
    FloatingIp4.new(
      PriceMonthly6.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    ),
    [
      FloatingIp5.new(
        [
          Price6.new(
            'fsn1',
            PriceMonthly7.new(
              '1.1900000000000000',
              '1.0000000000'
            )
          )
        ],
        Type48Enum::IPV4
      )
    ],
    Image3.new(
      PricePerGbMonth.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    ),
    [
      LoadBalancerType6.new(
        1,
        'lb11',
        [
          Price7.new(
            'fsn1',
            PriceHourly6.new(
              '1.1900000000000000',
              '1.0000000000'
            ),
            PriceMonthly8.new(
              '1.1900000000000000',
              '1.0000000000'
            )
          )
        ]
      )
    ],
    [
      PrimaryIp.new(
        [
          Price8.new(
            'fsn1',
            PriceHourly7.new(
              '1.1900000000000000',
              '1.0000000000'
            ),
            PriceMonthly9.new(
              '1.1900000000000000',
              '1.0000000000'
            )
          )
        ],
        Type49Enum::IPV4
      )
    ],
    ServerBackup.new(
      '20.0000000000'
    ),
    [
      ServerTypes2.new(
        4,
        'cx11',
        [
          Price9.new(
            'fsn1',
            PriceHourly8.new(
              '1.1900000000000000',
              '1.0000000000'
            ),
            PriceMonthly10.new(
              '1.1900000000000000',
              '1.0000000000'
            )
          )
        ]
      )
    ],
    Traffic.new(
      PricePerTb.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    ),
    '19.000000',
    Volume.new(
      PricePerGbMonth.new(
        '1.1900000000000000',
        '1.0000000000'
      )
    )
  )
)
```



