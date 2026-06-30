# Markets

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/spotify/portal/#/ruby/x-redirect/JTI0bSUyRk1hcmtldHM

*This model accepts additional fields of type Object.*


# Class Name

`Markets`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `markets` | `Array[String]` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
markets = Markets.new(
  markets: [
    'CA',
    'BR',
    'IT'
  ],
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



