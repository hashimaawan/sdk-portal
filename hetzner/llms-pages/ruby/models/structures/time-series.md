# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/#/ruby/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `values` | Array[Array[Float \| String]] | Required | This is 2d Array of a container for one-of cases. |


# Example

```ruby
time_series = TimeSeries.new(
  [
    [
      161.02,
      161.03
    ],
    [
      161.02,
      161.03
    ]
  ]
)
```



