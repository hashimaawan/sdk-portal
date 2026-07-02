# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q

*This model accepts additional fields of type Object.*


# Class Name

`StartSessionRequest`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1024` |
| `work_group` | `String` | Required | **Constraints**: *Pattern*: `[a-zA-Z0-9._-]{1,128}` |
| `engine_configuration` | [`EngineConfiguration1`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/llms-pages/ruby/models/structures/engine-configuration-1.md) | Required | - |
| `notebook_version` | `String` | Optional | **Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `session_idle_timeout_in_minutes` | `Integer` | Optional | **Constraints**: `>= 1`, `<= 480` |
| `client_request_token` | `String` | Optional | **Constraints**: *Minimum Length*: `32`, *Maximum Length*: `128` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |


# Example

```ruby
start_session_request = StartSessionRequest.new(
  work_group: 'WorkGroup4',
  engine_configuration: EngineConfiguration1.new(
    max_concurrent_dpus: 94,
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
  ),
  description: 'Description6',
  notebook_version: 'NotebookVersion6',
  session_idle_timeout_in_minutes: 78,
  client_request_token: 'ClientRequestToken6',
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



