# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-type.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_types_response1 = LoadBalancerTypesResponse1.new(
  load_balancer_type: LoadBalancerType.new(
    deprecated: 'deprecated2',
    description: 'description4',
    id: 205.06,
    max_assigned_certificates: 211.64,
    max_connections: 136.32,
    max_services: 199.18,
    max_targets: 152.52,
    name: 'name6',
    prices: [
      Price.new(
        location: 'location8',
        price_hourly: PriceHourly.new(
          gross: 'gross4',
          net: 'net2',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        price_monthly: PriceMonthly.new(
          gross: 'gross2',
          net: 'net0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Price.new(
        location: 'location8',
        price_hourly: PriceHourly.new(
          gross: 'gross4',
          net: 'net2',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        price_monthly: PriceMonthly.new(
          gross: 'gross2',
          net: 'net0',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      Price.new(
        location: 'location8',
        price_hourly: PriceHourly.new(
          gross: 'gross4',
          net: 'net2',
          additional_properties: {
            'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
          }
        ),
        price_monthly: PriceMonthly.new(
          gross: 'gross2',
          net: 'net0',
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
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



