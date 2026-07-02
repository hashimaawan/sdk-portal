# Floating Ip 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkZsb2F0aW5nSXAx

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`FloatingIp1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `droplet` | Object \| nil \| [Droplet](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/droplet.md) | Optional | This is a container for any-of cases. |
| `ip` | `String` | Optional | The public IP address of the floating IP. It also serves as its identifier. |
| `locked` | `TrueClass \| FalseClass` | Optional | A boolean value indicating whether or not the floating IP has pending actions preventing new ones from being submitted. |
| `project_id` | `UUID \| String` | Optional | The UUID of the project to which the reserved IP currently belongs. |
| `region` | [`Region`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/region.md) | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
floating_ip1 = FloatingIp1.new(
  droplet: { 'key1' => 'val1', 'key2' => 'val2' },
  ip: '45.55.96.47',
  locked: true,
  project_id: '746c6152-2fa2-11ed-92d3-27aaa54e4988',
  region: Region.new(
    available: false,
    features: [
      'features7',
      'features8',
      'features9'
    ],
    name: 'name6',
    sizes: [
      'sizes6'
    ],
    slug: 'slug0',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



