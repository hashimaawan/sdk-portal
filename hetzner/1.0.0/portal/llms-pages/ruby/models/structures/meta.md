# Meta

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRk1ldGE

*This model accepts additional fields of type Object.*


# Class Name

`Meta`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `pagination` | [`Pagination`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/llms-pages/ruby/models/structures/pagination.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
meta = Meta.new(
  pagination: Pagination.new(
    last_page: 4,
    next_page: 4,
    page: 3,
    per_page: 25,
    previous_page: 2,
    total_entries: 100,
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



