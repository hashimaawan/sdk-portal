# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0

*This model accepts additional fields of type Object.*


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_groups` | [`Array[WorkGroupSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_work_groups_output = ListWorkGroupsOutput.new(
  work_groups: [
    WorkGroupSummary.new(
      name: 'Name4',
      state: WorkGroupState1::ENABLED,
      description: 'Description0',
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
  ],
  next_token: 'NextToken2',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



