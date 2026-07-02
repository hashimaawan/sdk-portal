# Progress

Source: https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/#/ruby/x-redirect/JTI0bSUyRlByb2dyZXNz

*This model accepts additional fields of type [Object](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md).*


# Class Name

`Progress`


# Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `error_steps` | `Integer` | Optional | - |
| `pending_steps` | `Integer` | Optional | - |
| `running_steps` | `Integer` | Optional | - |
| `steps` | [`Array[AStepThatIsRunAsPartOfTheDeploymentSLifecycle]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `success_steps` | `Integer` | Optional | - |
| `summary_steps` | [`Array[AStepThatIsRunAsPartOfTheDeploymentSLifecycle]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/a-step-that-is-run-as-part-of-the-deployment-s-lifecycle.md) | Optional | - |
| `total_steps` | `Integer` | Optional | - |
| `additional_properties` | [`Hash[String, Object]`](https://raw.githubusercontent.com/hashimaawan/sdk-portal/main/digitalocean/2.0/portal/llms-pages/ruby/models/structures/object.md) | Optional | - |


# Example

```ruby
progress = Progress.new(
  error_steps: 3,
  pending_steps: 2,
  running_steps: 2,
  steps: [
    AStepThatIsRunAsPartOfTheDeploymentSLifecycle.new(
      component_name: 'component_name0',
      ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      message_base: 'message_base4',
      name: 'name2',
      reason: Reason.new(
        code: 'code2',
        message: 'message4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AStepThatIsRunAsPartOfTheDeploymentSLifecycle.new(
      component_name: 'component_name0',
      ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      message_base: 'message_base4',
      name: 'name2',
      reason: Reason.new(
        code: 'code2',
        message: 'message4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    ),
    AStepThatIsRunAsPartOfTheDeploymentSLifecycle.new(
      component_name: 'component_name0',
      ended_at: DateTimeHelper.from_rfc3339('2016-03-13T12:52:32.123Z'),
      message_base: 'message_base4',
      name: 'name2',
      reason: Reason.new(
        code: 'code2',
        message: 'message4',
        additional_properties: {
          'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
        }
      ),
      additional_properties: {
        'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
      }
    )
  ],
  success_steps: 4,
  total_steps: 5,
  additional_properties: {
    'exampleAdditionalProperty' => JSON.parse('{"key1":"val1","key2":"val2"}')
  }
)
```



