# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlBhZ2luYXRpb24


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


# Example

```ruby
pagination = Pagination.new(
  4,
  4,
  3,
  25,
  2,
  100
)
```



