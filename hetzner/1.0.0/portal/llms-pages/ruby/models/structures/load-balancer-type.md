# Load Balancer Type

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRkxvYWRCYWxhbmNlclR5cGU

*This model accepts additional fields of type Object.*


# Class Name

`LoadBalancerType`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `deprecated` | `String` | Required | Point in time when the Load Balancer type is deprecated (in ISO-8601 format) |
| `description` | `String` | Required | Description of the Load Balancer type |
| `id` | `Float` | Required | ID of the Load Balancer type |
| `max_assigned_certificates` | `Float` | Required | Number of SSL Certificates that can be assigned to a single Load Balancer |
| `max_connections` | `Float` | Required | Number of maximum simultaneous open connections |
| `max_services` | `Float` | Required | Number of services a Load Balancer of this type can have |
| `max_targets` | `Float` | Required | Number of targets a single Load Balancer can have |
| `name` | `String` | Required | Unique identifier of the Load Balancer type |
| `prices` | [`Array[Price]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/price.md) | Required | Prices in different network zones |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
load_balancer_type = LoadBalancerType.new(
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
```



