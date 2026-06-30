# Url

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/1password/#/ruby/x-redirect/JTI0bSUyRlVybA

*This model accepts additional fields of type Object.*


# Class Name

`Url`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `href` | `String` | Required | - |
| `label` | `String` | Optional | - |
| `primary` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
url = Url.new(
  href: 'href6',
  label: 'label4',
  primary: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



