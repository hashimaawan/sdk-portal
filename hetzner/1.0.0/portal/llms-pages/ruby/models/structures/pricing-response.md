# Pricing Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlByaWNpbmclMjUyMFJlc3BvbnNl

*This model accepts additional fields of type Object.*


# Class Name

`PricingResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pricing` | [`Pricing`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/pricing.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
pricing_response = PricingResponse.new(
  pricing: Pricing.new(
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



