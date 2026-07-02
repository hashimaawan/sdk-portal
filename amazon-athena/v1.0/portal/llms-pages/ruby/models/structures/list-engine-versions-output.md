# List Engine Versions Output

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkxpc3RFbmdpbmVWZXJzaW9uc091dHB1dA


# Class Name

`ListEngineVersionsOutput`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `engine_versions` | [`Array[EngineVersion]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-version.md) | Optional | **Constraints**: *Minimum Items*: `0`, *Maximum Items*: `10` |
| `next_token` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |


# Example

```ruby
list_engine_versions_output = ListEngineVersionsOutput.new(
  [
    EngineVersion.new(
      'SelectedEngineVersion2',
      'EffectiveEngineVersion2'
    ),
    EngineVersion.new(
      'SelectedEngineVersion2',
      'EffectiveEngineVersion2'
    )
  ],
  'NextToken2'
)
```



