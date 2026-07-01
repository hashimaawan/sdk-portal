# Pagination

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/giphy/1.0/portal/#/ruby/x-redirect/JTI0bSUyRlBhZ2luYXRpb24

The Pagination Object contains information relating to the number of total results available as well as the number of results fetched and their relative positions.


# Class Name

`Pagination`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `count` | `Integer` | Optional | Total number of items returned. |
| `offset` | `Integer` | Optional | Position in pagination. |
| `total_count` | `Integer` | Optional | Total number of items available. |


# Example

```ruby
pagination = Pagination.new(
  25,
  75,
  250
)
```



