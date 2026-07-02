# Floating Ip

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXA

An objects containing information about a resource associated with a Droplet.

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`FloatingIp`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cost` | `String` | Optional | The cost of the resource in USD per month if the resource is retained after the Droplet is destroyed. |
| `id` | `String` | Optional | The unique identifier for the resource associated with the Droplet. |
| `name` | `String` | Optional | The name of the resource associated with the Droplet. |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
floating_ip = FloatingIp.new(
  cost: '0.05',
  id: '61486916',
  name: 'ubuntu-s-1vcpu-1gb-nyc1-01-1585758823330',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



