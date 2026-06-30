# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `String` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 |
| `floating_ip` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month |
| `floating_ips` | [`Array[FloatingIp5]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type |
| `image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/image-3.md) | Required | The cost of Image per GB/month |
| `load_balancer_types` | [`Array[LoadBalancerType6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type |
| `primary_ips` | [`Array[PrimaryIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location |
| `server_backup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage |
| `server_types` | [`Array[ServerTypes2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type |
| `traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/traffic.md) | Required | The cost of additional traffic per TB |
| `vat_rate` | `String` | Required | The VAT rate used for calculating prices with VAT |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/llms-pages/ruby/models/structures/volume.md) | Required | The cost of Volume per GB/month |


# Example

```ruby
pricing = Pricing.new(
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
```



