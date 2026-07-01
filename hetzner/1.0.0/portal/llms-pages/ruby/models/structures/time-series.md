# Time Series

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/hetzner/1.0.0/portal/#/ruby/x-redirect/JTI0bSUyRlRpbWVTZXJpZXM

*This model accepts additional fields of type Object.*


# Class Name

`TimeSeries`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `values` | Array[Array[Float \| String]] | Required | This is 2d Array of a container for one-of cases. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
time_series = TimeSeries.new(
  values: [
    [
      161.02,
      161.03
    ],
    [
      161.02,
      161.03
    ]
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



