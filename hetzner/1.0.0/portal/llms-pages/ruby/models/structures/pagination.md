# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

*This model accepts additional fields of type Object.*


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `last_page` | `Float` | Required | ID of the last page available. Can be null if the current page is the last one. |
| `next_page` | `Float` | Required | ID of the next page. Can be null if the current page is the last one. |
| `page` | `Float` | Required | Current page number |
| `per_page` | `Float` | Required | Maximum number of items shown per page in the response |
| `previous_page` | `Float` | Required | ID of the previous page. Can be null if the current page is the first one. |
| `total_entries` | `Float` | Required | The total number of entries that exist in the database for this query. Nullable if unknown. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
pagination = Pagination.new(
  last_page: 4,
  next_page: 4,
  page: 3,
  per_page: 25,
  previous_page: 2,
  total_entries: 100,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



