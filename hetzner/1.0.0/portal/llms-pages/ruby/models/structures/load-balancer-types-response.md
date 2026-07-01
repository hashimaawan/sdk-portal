# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_types` | [`Array[LoadBalancerType]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-type.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_types_response = LoadBalancerTypesResponse.new(
  load_balancer_types: [
    LoadBalancerType.new(
      deprecated: '2016-01-30T23:50:00+00:00',
      description: 'LB11',
      id: 1,
      max_assigned_certificates: 10,
      max_connections: 20000,
      max_services: 5,
      max_targets: 25,
      name: 'lb11',
      prices: [
        Price.new(
          location: 'fsn1',
          price_hourly: PriceHourly.new(
            gross: '1.1900000000000000',
            net: '1.0000000000',
            additional_properties: {
              'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
            }
          ),
          price_monthly: PriceMonthly.new(
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
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



