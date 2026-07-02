# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA

*This model accepts additional fields of type Object.*


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engine_versions` | [`Array[EngineVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
list_engine_versions_output = ListEngineVersionsOutput.new(
  engine_versions: [
    EngineVersion.new(
      selected_engine_version: 'SelectedEngineVersion2',
      effective_engine_version: 'EffectiveEngineVersion2',
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    EngineVersion.new(
      selected_engine_version: 'SelectedEngineVersion2',
      effective_engine_version: 'EffectiveEngineVersion2',
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



