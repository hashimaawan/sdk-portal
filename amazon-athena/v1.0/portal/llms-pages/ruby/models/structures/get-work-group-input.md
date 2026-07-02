# Get Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkdldFdvcmtHcm91cElucHV0

*This model accepts additional fields of type Object.*


# Class Name

`GetWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
get_work_group_input = GetWorkGroupInput.new(
  work_group: 'WorkGroup0',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



