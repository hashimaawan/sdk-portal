# Delete Work Group Input

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkRlbGV0ZVdvcmtHcm91cElucHV0

*This model accepts additional fields of type Object.*


# Class Name

`DeleteWorkGroupInput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `recursive_delete_option` | `TrueClass \| FalseClass` | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
delete_work_group_input = DeleteWorkGroupInput.new(
  work_group: 'WorkGroup8',
  recursive_delete_option: false,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



