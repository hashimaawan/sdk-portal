# Datum

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkRhdHVt

A piece of data (a field in the table).

*This model accepts additional fields of type Object.*


# Class Name

`Datum`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `var_char_value` | `String` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
datum = Datum.new(
  var_char_value: 'VarCharValue8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



