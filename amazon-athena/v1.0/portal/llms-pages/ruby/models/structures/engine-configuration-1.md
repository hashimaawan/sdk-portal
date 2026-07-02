# Engine Configuration 1

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24x

*This model accepts additional fields of type Object.*


# Class Name

`EngineConfiguration1`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `coordinator_dpu_size` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `max_concurrent_dpus` | `Integer` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `default_executor_dpu_size` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `additional_configs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/additional-configs.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
engine_configuration1 = EngineConfiguration1.new(
  max_concurrent_dpus: 96,
  coordinator_dpu_size: 1,
  default_executor_dpu_size: 1,
  additional_configs: AdditionalConfigs.new(
    additional_properties: {
      'exampleAdditionalProperty' => 'AdditionalConfigs_additionalProperties5'
    }
  ),
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



