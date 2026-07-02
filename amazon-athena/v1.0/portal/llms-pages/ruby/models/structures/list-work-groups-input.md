# List Work Groups Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzSW5wdXQ

*This model accepts additional fields of type Object.*


# Class Name

`ListWorkGroupsInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `max_results` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 50` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_work_groups_input = ListWorkGroupsInput.new(
  next_token: 'NextToken8',
  max_results: 50,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



