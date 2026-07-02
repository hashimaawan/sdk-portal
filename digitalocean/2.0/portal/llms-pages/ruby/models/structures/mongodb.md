# Mongodb

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRk1vbmdvZGI

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Mongodb`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `regions` | `Array[String]` | Optional, Read-only | An array of strings containing the names of available regions |
| `versions` | `Array[String]` | Optional, Read-only | An array of strings containing the names of available regions |
| `layouts` | [`Array[Layout]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/layout.md) | Optional, Read-only | An array of objects, each indicating the node sizes (otherwise referred to as slugs) that are available with various numbers of nodes in the database cluster. Each slugs denotes the node's identifier, CPU, and RAM (in that order). |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
mongodb = Mongodb.new(
  regions: [
    'ams3',
    'blr1'
  ],
  versions: [
    '4.4',
    '5.0'
  ],
  layouts: [
    Layout.new(
      num_nodes: 190,
      sizes: [
        'sizes2',
        'sizes3'
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    Layout.new(
      num_nodes: 190,
      sizes: [
        'sizes2',
        'sizes3'
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



