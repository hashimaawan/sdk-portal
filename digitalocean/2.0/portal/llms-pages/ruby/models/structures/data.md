# Data

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdGE

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Data`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `result` | [`Array[Result]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/result.md) | Required | Result of query. |
| `result_type` | `String` | Required, Constant | **Value**: `'matrix'` |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
data = Data.new(
  result: [
    Result.new(
      metric: {
        'host_id' => '19201920'
      },
      values: [
        [
          1435781430,
          '1'
        ],
        [
          1435781445,
          '1'
        ]
      ],
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  result_type: 'matrix',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



