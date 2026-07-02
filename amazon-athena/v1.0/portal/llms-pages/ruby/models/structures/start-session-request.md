# Start Session Request

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/amazon-athena/v1.0/portal/#/ruby/x-redirect/JTI0bSUyRlN0YXJ0U2Vzc2lvblJlcXVlc3Q


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


# Example

```ruby
start_session_request = StartSessionRequest.new(
  'WorkGroup4',
  EngineConfiguration1.new(
    94,
    1,
    1,
    AdditionalConfigs.new
  ),
  'Description6',
  'NotebookVersion6',
  78,
  'ClientRequestToken6'
)
```



