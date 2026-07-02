# Engine Configuration

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRkVuZ2luZUNvbmZpZ3VyYXRpb24

Contains data processing unit (DPU) configuration settings and parameter mappings for a notebook engine.


# Class Name

`EngineConfiguration`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `coordinator_dpu_size` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `max_concurrent_dpus` | `Integer` | Required | **Constraints**: `>= 2`, `<= 5000` |
| `default_executor_dpu_size` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 1` |
| `additional_configs` | [`AdditionalConfigs`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/additional-configs.md) | Optional | - |


# Example

```ruby
engine_configuration = EngineConfiguration.new(
  132,
  1,
  1,
  AdditionalConfigs.new
)
```



