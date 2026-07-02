# Layout

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkxheW91dA

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Layout`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `num_nodes` | `Integer` | Optional | - |
| `sizes` | `Array[String]` | Optional, Read-only | An array of objects containing the slugs available with various node counts |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
layout = Layout.new(
  num_nodes: 1,
  sizes: [
    'db-s-1vcpu-1gb',
    'db-s-1vcpu-2gb'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



