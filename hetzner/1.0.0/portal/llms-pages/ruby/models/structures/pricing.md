# Pricing

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNpbmc


# Class Name

`Pricing`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `currency` | `String` | Required | Currency the returned prices are expressed in, coded according to ISO 4217 |
| `floating_ip` | [`FloatingIp4`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/floating-ip-4.md) | Required | The cost of one Floating IP per month |
| `floating_ips` | [`Array[FloatingIp5]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/floating-ip-5.md) | Required | Costs of Floating IPs types per Location and type |
| `image` | [`Image3`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/image-3.md) | Required | The cost of Image per GB/month |
| `load_balancer_types` | [`Array[LoadBalancerType6]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-type-6.md) | Required | Costs of Load Balancer types per Location and type |
| `primary_ips` | [`Array[PrimaryIp]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/primary-ip.md) | Required | Costs of Primary IPs types per Location |
| `server_backup` | [`ServerBackup`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-backup.md) | Required | Will increase base Server costs by specific percentage |
| `server_types` | [`Array[ServerTypes2]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/server-types-2.md) | Required | Costs of Server types per Location and type |
| `traffic` | [`Traffic`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/traffic.md) | Required | The cost of additional traffic per TB |
| `vat_rate` | `String` | Required | The VAT rate used for calculating prices with VAT |
| `volume` | [`Volume`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/volume.md) | Required | The cost of Volume per GB/month |


# Example

```ruby
pricing = Pricing.new(
  currency: 'EUR',
  floating_ip: FloatingIp4.new(
    price_monthly: PriceMonthly6.new(
      gross: '1.1900000000000000',
      net: '1.0000000000',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  floating_ips: [
    FloatingIp5.new(
      prices: [
        Price6.new(
          location: 'fsn1',
          price_monthly: PriceMonthly7.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      type: Type48::IPV4,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  image: Image3.new(
    price_per_gb_month: PricePerGbMonth.new(
      gross: '1.1900000000000000',
      net: '1.0000000000',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  load_balancer_types: [
    LoadBalancerType6.new(
      id: 1,
      name: 'lb11',
      prices: [
        Price7.new(
          location: 'fsn1',
          price_hourly: PriceHourly6.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          price_monthly: PriceMonthly8.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  primary_ips: [
    PrimaryIp.new(
      prices: [
        Price8.new(
          location: 'fsn1',
          price_hourly: PriceHourly7.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          price_monthly: PriceMonthly9.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      type: Type49::IPV4,
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  server_backup: ServerBackup.new(
    percentage: '20.0000000000',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  server_types: [
    ServerTypes2.new(
      id: 4,
      name: 'cx11',
      prices: [
        Price9.new(
          location: 'fsn1',
          price_hourly: PriceHourly8.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          price_monthly: PriceMonthly10.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        )
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  traffic: Traffic.new(
    price_per_tb: PricePerTb.new(
      gross: '1.1900000000000000',
      net: '1.0000000000',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  vat_rate: '19.000000',
  volume: Volume.new(
    price_per_gb_month: PricePerGbMonth.new(
      gross: '1.1900000000000000',
      net: '1.0000000000',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  )
)
```



