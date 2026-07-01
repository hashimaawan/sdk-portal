# Load Balancer Types Response

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2U


# Class Name

`LoadBalancerTypesResponse`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_types` | [`Array[LoadBalancerType]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-type.md) | Required | - |


# Example

```ruby
load_balancer_types_response = LoadBalancerTypesResponse.new(
  [
    LoadBalancerType.new(
      '2016-01-30T23:50:00+00:00',
      'LB11',
      1,
      10,
      20000,
      5,
      25,
      'lb11',
      [
        Price.new(
          'fsn1',
          PriceHourly.new(
            '1.1900000000000000',
            '1.0000000000'
          ),
          PriceMonthly.new(
            '1.1900000000000000',
            '1.0000000000'
          )
        )
      ]
    )
  ]
)
```



