# List Work Groups Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RXb3JrR3JvdXBzT3V0cHV0


# Class Name

`ListWorkGroupsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `work_groups` | [`Array[WorkGroupSummary]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/work-group-summary.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `50` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
list_work_groups_output = ListWorkGroupsOutput.new(
  [
    WorkGroupSummary.new(
      'Name4',
      WorkGroupState1Enum::ENABLED,
      'Description0',
      DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      EngineVersion1.new(
        'SelectedEngineVersion4',
        'EffectiveEngineVersion6'
      )
    )
  ],
  'NextToken2'
)
```



