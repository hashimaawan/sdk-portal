# Work Group Summary

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRldvcmtHcm91cFN1bW1hcnk

The summary information for the workgroup, which includes its name, state, description, and the date and time it was created.

*This model accepts additional fields of type Object.*


# Class Name

`WorkGroupSummary`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `state` | [`WorkGroupState1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/enumerations/work-group-state-1.md) | Optional | - |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `0`, *Maximum Length*: `1024` |
| `creation_time` | `DateTime` | Optional | - |
| `engine_version` | [`EngineVersion1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
work_group_summary = WorkGroupSummary.new(
  name: 'Name2',
  state: WorkGroupState1::ENABLED,
  description: 'Description4',
  creation_time: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
  engine_version: EngineVersion1.new(
    selected_engine_version: 'SelectedEngineVersion4',
    effective_engine_version: 'EffectiveEngineVersion6',
    additional_properties: {
      'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



