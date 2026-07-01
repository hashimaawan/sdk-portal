# Load Balancer Types Response 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWQlMjUyMEJhbGFuY2VyJTI1MjBUeXBlcyUyNTIwUmVzcG9uc2Ux


# Class Name

`LoadBalancerTypesResponse1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `load_balancer_type` | [`LoadBalancerType`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/load-balancer-type.md) | Optional | - |


# Example

```ruby
load_balancer_types_response1 = LoadBalancerTypesResponse1.new(
  LoadBalancerType.new(
    'deprecated2',
    'description4',
    205.06,
    211.64,
    136.32,
    199.18,
    152.52,
    'name6',
    [
      Price.new(
        'location8',
        PriceHourly.new(
          'gross4',
          'net2'
        ),
        PriceMonthly.new(
          'gross2',
          'net0'
        )
      ),
      Price.new(
        'location8',
        PriceHourly.new(
          'gross4',
          'net2'
        ),
        PriceMonthly.new(
          'gross2',
          'net0'
        )
      ),
      Price.new(
        'location8',
        PriceHourly.new(
          'gross4',
          'net2'
        ),
        PriceMonthly.new(
          'gross2',
          'net0'
        )
      )
    ]
  )
)
```



