# Engine Version 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkVuZ2luZVZlcnNpb24x

*This model accepts additional fields of type Object.*


# Class Name

`EngineVersion1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `selected_engine_version` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `effective_engine_version` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
engine_version1 = EngineVersion1.new(
  selected_engine_version: 'SelectedEngineVersion8',
  effective_engine_version: 'EffectiveEngineVersion8',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



